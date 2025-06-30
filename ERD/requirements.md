# Entity-Relationship Diagram (ERD)

## Objective:
Design an ERD to model an Airbnb-like system with users, properties, bookings, payments, and reviews.

## Entities:

1. **Users**
   - id (PK)
   - name
   - email
   - password
   - role (host/guest)

2. **Properties**
   - id (PK)
   - title
   - description
   - location
   - price_per_night
   - host_id (FK → Users)

3. **Bookings**
   - id (PK)
   - user_id (FK → Users)
   - property_id (FK → Properties)
   - check_in_date
   - check_out_date
   - total_price

4. **Reviews**
   - id (PK)
   - booking_id (FK → Bookings)
   - rating
   - comment

5. **Payments**
   - id (PK)
   - booking_id (FK → Bookings)
   - amount
   - payment_method
   - payment_status

## Relationships:

- A **User** can make many **Bookings**.
- A **User** (as a host) can own many **Properties**.
- A **Property** can have many **Bookings**.
- Each **Booking** has one **Review** and one **Payment**.

## ER Diagram:

_Visual diagram is available in this directory as `airbnb_erd.png` or `.drawio`._
