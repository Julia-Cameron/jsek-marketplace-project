# JSEK Marketplace

JSEK Marketplace is a responsive static marketplace demo for buying and selling electronics. It includes separate buyer, seller, vendor, and admin entry points while keeping a shared glass-style visual theme.

This project was developed as a collaborative software engineering project using Agile practices, Git version control, and Jira for planning, task tracking, and sprint coordination.

## My Contributions

I designed and implemented the main customer-facing flow and its validation logic:

- Created the marketplace landing page in `index.html`
- Created the account registration page in `signup.html`
- Created the login page in `login.html`
- Created the secure checkout page in `checkout.html`
- Added checkout validation for cardholder name, card number, expiry date, CVV, and payment method selection
- Added PayPal and credit-card checkout states
- Added receipt generation with subtotal, 13% HST, total payment, and print/email options
- Added responsive layout and padding adjustments for desktop and mobile screens

The remaining vendor, admin, and support pages were integrated into the same navigation and visual theme as part of the complete marketplace demo.

## Features

- Portal selection from the home page
- Local demo account registration with role selection
- Login with remember-me support and role-based dashboard routing
- Checkout with credit-card validation and PayPal flow selection
- Receipt generation with tax calculation and print/email delivery options
- Vendor inventory view with stock status
- Admin dashboard with account filters and session protection
- Technical support ticket confirmation and password-reset request confirmation
- Responsive layout for desktop and mobile screens

## Run Locally

No build tools or server are required. Open `index.html` in a browser, or use VS Code Live Server for easier navigation between pages.

The demo stores accounts and the active session in browser `localStorage` using `jsek_users`, `currentUser`, and `isLoggedIn`. This is front-end demonstration logic only and must not be used for real passwords or payments.

## Main Pages

| Page | Purpose |
| --- | --- |
| `index.html` | Marketplace portal selection |
| `signup.html` | Create a demo account and choose a role |
| `login.html` | Sign in and route to the appropriate area |
| `checkout.html` | Demonstration checkout flow |
| `receipt.html` | Payment receipt with HST calculation and delivery options |
| `vendor_inventory.html` | Vendor stock overview |
| `admin_dashboard.html` | Admin account overview and filtering |
| `support.html` | Submit a support ticket |
| `forgot-password.html` | Request password-reset instructions |

## Project Team

- Emad Al Nounou
- Julia Cameron
- Khaled Al Akili
- Shefaa Alaghawani
