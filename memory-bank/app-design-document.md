# Food Ordering App – Application Design Documentation

## Application Goals

- Provide a seamless web-based platform for customers to browse, select, and order food online.
- Enable administrators to manage dishes, categories, orders, and users through a robust CMS.
- Ensure a responsive, accessible, and user-friendly experience across devices.

## User Flow

### Customer
1. **Browse Menu:** View food categories and dishes with details and prices.
2. **Add to Cart:** Select dishes and add them to a shopping cart.
3. **Place Order:** Review cart, provide contact details, and submit order (no payment integration yet).
4. **Order History:** View a history of past orders.

### Admin
1. **Login:** Secure authentication to access admin dashboard.
2. **Manage Content:** Add/edit/remove categories, dishes, and view/manage orders.
3. **User Management:** Manage customer and admin accounts.

## Key Features

### Front-end
- Dynamic food menu with categories and dish details.
- Cart functionality with add/remove/update operations.
- Order submission and order history views.
- Responsive UI using custom components, Radix UI, TailwindCSS, and Geist.
- Authentication flows for customers and admins.

### Back-end (Payload CMS)
- Collections for dishes, categories, users, and orders.
- Custom access controls for admin/customer roles.
- API endpoints for menu, cart, order, and user management.
- Plugins for SEO, search, redirects, and nested docs.

## Order Logic

- **Cart State:** Managed client-side, persisted across sessions.
- **Order Submission:** On checkout, cart data and user info are sent to Payload CMS, creating a new order entry.
- **Order History:** Orders are linked to user accounts; authenticated users can view their own order history.
- **Admin Review:** Admins can view and manage all orders via the CMS dashboard.

---
