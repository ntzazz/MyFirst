Enhance application that currently has no authentication or authorization.

Design and implement a secure, role-based user management module. All the persistent data should store as JSONs in local file system



Core Requirements



**Authentication**

* Require login for all application routes
* Use email/username + password
* Hash passwords using industry-standard hashing
* Implement session-based or token-based authentication
* Support logout and session invalidation



**Authorization**

* Implement Role-Based Access Control (RBAC)
* Roles: ADMIN, CONFIGURATOR, CONSUMER, REVIEWER, READ\_ONLY
* Enforce authorization checks on every protected API and UI route
* Block direct URL access without permission



**User Management (Admin Only)**

* Create users
* Update user details
* Activate / deactivate users
* Delete users (soft delete preferred)
* Assign and change user roles
* Prevent duplicate users (email unique)



**User Status Rules**

* User statuses: ACTIVE, INACTIVE, SUSPENDED
* Only ACTIVE users can log in
* Inactive or suspended users must be denied access



**Access Control**

* Deny all unauthenticated requests by default
* Validate authorization on every backend request
* Return proper HTTP status codes (401 / 403)



**Audit \& Logging**



* Log login and logout events
* Log user creation, update, deactivation, deletion
* Include timestamp and actor in logs
