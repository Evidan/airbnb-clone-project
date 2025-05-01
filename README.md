## Database design
🗃️ Database Design
This section outlines the core database entities and their relationships for the Airbnb Clone backend.

1. Users
Represents individuals using the platform as hosts or guests.

id (Primary Key): Unique identifier for the user.

email: User's email address (unique).

password: Encrypted password for authentication.

full_name: The full name of the user.

is_host: Boolean indicating whether the user is a host.

Relationships:

A user can own multiple properties.

A user can make multiple bookings.

A user can leave multiple reviews.

2. Properties
Represents a listing posted by a host.

id (Primary Key): Unique identifier for the property.

user_id (Foreign Key → Users): The host who owns this property.

title: Title or name of the property.

description: Detailed description of the property.

location: Address or location of the property.

Relationships:

A property belongs to one user (host).

A property can have multiple bookings.

A property can receive multiple reviews.

3. Bookings
Represents a reservation made by a guest.

id (Primary Key): Unique identifier for the booking.

user_id (Foreign Key → Users): Guest who made the booking.

property_id (Foreign Key → Properties): The property being booked.

check_in: Start date of the booking.

check_out: End date of the booking.

Relationships:

A booking belongs to one user (guest).

A booking belongs to one property.

A booking can be associated with one payment.

4. Payments
Handles transactions related to bookings.

id (Primary Key): Unique identifier for the payment.

booking_id (Foreign Key → Bookings): Booking for which the payment was made.

amount: Total payment amount.

payment_status: Status of the transaction (e.g., pending, completed).

payment_date: Date the payment was processed.

Relationships:

A payment belongs to one booking.

5. Reviews
Captures feedback left by guests.

id (Primary Key): Unique identifier for the review.

user_id (Foreign Key → Users): The guest who left the review.

property_id (Foreign Key → Properties): The property being reviewed.

rating: Numeric rating (e.g., 1-5).

comment: Text feedback.

Relationships:

A review belongs to one user.

A review belongs to one property.

