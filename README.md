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
- Added automatic card-network detection (Visa/Mastercard) as the card number is typed
- Added card number validation (Luhn checksum) and simulated decline scenarios (invalid card, insufficient funds)
- Added PayPal and credit-card checkout states
- Added receipt generation with subtotal, 13% HST, total payment, and print/email options
- Added responsive layout and padding adjustments for desktop and mobile screens

The remaining vendor, admin, and support pages were integrated into the same navigation and visual theme as part of the complete marketplace demo.

## Features

- Portal selection from the home page
- Local demo account registration with role selection
- Login with remember-me support and role-based dashboard routing
- Checkout with credit-card validation, live Visa/Mastercard detection, and PayPal flow selection
- Receipt generation with tax calculation and print/email delivery options
- Vendor inventory view with stock status
- Admin dashboard with account filters and session protection
- Technical support ticket confirmation and password-reset request confirmation
- Responsive layout for desktop and mobile screens

## Checkout Card Testing

The checkout form (`checkout.html`) validates card numbers with a Luhn checksum, detects the card network (Visa/Mastercard) live as digits are typed, and simulates bank decline responses for specific test numbers. All numbers below are fake/publicly-used test values — no real payment data is involved.

| Card number | Expected result |
| --- | --- |
| `4242 4242 4242 4242` | Valid Visa — passes validation and completes payment |
| `5555 5555 5555 4444` | Valid Mastercard — passes validation and completes payment |
| `4242 4242 4242 4241` | Invalid card number — fails the Luhn checksum, shows "Invalid card number" error |
| `4000 0000 0000 9995` | Valid Visa, simulated decline — shows "insufficient funds" error |
| `4000 0000 0000 0002` | Valid Visa, simulated decline — shows "declined by the issuing bank" error |

To test: open `checkout.html`, select Credit Card, enter any name/future expiry/3-digit CVV, then type one of the numbers above into the card number field. The Visa/Mastercard label appears automatically to the right of the field as you type, and submitting the form shows the corresponding success or error message.


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
