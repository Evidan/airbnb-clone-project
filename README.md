🔐 API Security
Securing the backend APIs is essential to protect sensitive user data, prevent unauthorized access, and ensure the integrity of financial transactions. The Airbnb Clone implements multiple layers of security to safeguard its system and users.

🔑 Authentication
All users must authenticate using secure login credentials. JWT (JSON Web Tokens) or session-based authentication will be used to verify user identities before accessing protected endpoints.

Why it matters: Ensures that only legitimate users can access their accounts and prevents impersonation or data breaches.

🛡️ Authorization
Role-based access control (RBAC) will be enforced to restrict access to specific resources. For instance, only hosts can create or modify properties, and only guests who made bookings can leave reviews.

Why it matters: Prevents users from performing unauthorized actions and maintains data integrity across the platform.

🚫 Rate Limiting
The API will implement rate limiting to prevent abuse, such as brute-force login attempts or denial-of-service attacks. Throttling policies will restrict the number of requests per user/IP over a given time period.

Why it matters: Protects the backend from spam, malicious traffic, and resource exhaustion.

🔒 Data Encryption
Sensitive data such as passwords and payment information will be encrypted at rest and in transit using HTTPS and secure hashing algorithms like bcrypt.

Why it matters: Protects user credentials and financial data from being intercepted or leaked during communication or storage.

✅ Input Validation & Sanitization
All inputs will be validated and sanitized to prevent injection attacks (e.g., SQL injection, XSS). DRF serializers and Django model constraints will enforce data integrity.

Why it matters: Blocks common attack vectors that could compromise the system or corrupt the database.

