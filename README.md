Assignment: Role-Based Navigation in an E-Commerce Admin Panel
Problem Statement:
You are developing an Admin Panel for an E-Commerce platform. The platform has three types of users:
1. Admin - Full access to all sections.
2. Manager - Access to product management and order management but not user
management.
3. Customer Support - Access only to order management.
Your task is to implement navigation restrictions using Angular Guards (CanActivate and CanActivateChild) to ensure that users can only access the sections they are authorized
Requirements:
• Use CanActivate Guard to protect the main admin routes based on user roles
• Use CanActivateChild Guard to restrict access to specific child routes under the admin panel.
• Store user roles in a mock authentication service (AuthService).
• Redirect unauthorized users to a 403 Forbidden page if they try to access restricted pages.