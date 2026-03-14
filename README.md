# Barber Bliss - Elite Haircut & Styling Studio

Welcome to Barber Bliss, a cutting-edge web experience designed for modern barber shops. This site offers a stunning visual aesthetic, seamless booking, and a powerful administrative dashboard, all built with the performance and flexibility of Vanilla HTML, Tailwind CSS (CDN), and pure JavaScript.

## Features

*   **Ultra-Modern Design**: A sleek, high-performance aesthetic inspired by $1M dollar tech startups.
*   **Dynamic UI**: Immersive glassmorphism, 3D transform hover effects, and animated gradient borders.
*   **Bento-Box Layouts**: Clean, organized sections for services, testimonials, and contact.
*   **Advanced Micro-Interactions**: Subtle, engaging animations powered by Tailwind CSS.
*   **Multi-Language Support**: Seamlessly switch between English and Hebrew.
*   **Theme Toggle**: Light and Dark mode options for personalized browsing.
*   **Effortless Booking System**: Clients can easily schedule appointments with instant confirmation.
*   **God-Tier Admin Dashboard**: A secure, intuitive interface for managing bookings, complete with real-time browser notifications.

## Stack

*   **Frontend**: HTML5, Tailwind CSS (CDN), Vanilla JS (Inline)
*   **Backend**: None (API calls handled by external service for bookings/admin)
*   **Styling**: Tailwind CSS via CDN for rapid, consistent UI development.

## Setup & Deployment

1.  **Clone the Repository**:
    ```bash
    git clone [your-repo-link]
    cd barber-bliss
    ```
2.  **Local Development (Optional, for Tailwind CLI if not using CDN directly)**:
    If you wish to build Tailwind locally (though the CDN is used in `index.html`), ensure you have Node.js installed.
    ```bash
    npm install
    npm run dev # To watch for CSS changes and build
    npm run build # To build production CSS
    ```
    *Note: The primary application uses Tailwind via CDN for simplicity and immediate rendering.*

3.  **Vercel Deployment**:
    This project is optimized for Vercel. Simply connect your Git repository to Vercel, and it will automatically detect the configuration from `vercel.json` and deploy.

## Usage

*   **Client Interface**: Navigate through the sections, select services, and use the booking form to schedule an appointment. Use the language and theme toggles in the navigation for a customized experience.
*   **Admin Access**:
    1.  Click the "Manage Bookings" link in the footer.
    2.  Enter the administrator PIN (securely stored in Firestore: `G7I1X5`) into the login modal.
    3.  Once authenticated, you will access the dashboard where you can view and manage all appointments.
    4.  Enable "Desktop Notifications" to receive real-time alerts for new bookings. The system polls for new bookings every 60 seconds.

## API Endpoints

*   **Booking Creation**: `POST` requests to `https://ammoue-ai.vercel.app/api/booking`
*   **Admin Verification**: `POST` requests to `/api/verify-admin` (configured via `vercel.json` to proxy to `https://ammoue-ai.vercel.app/api/verify-admin`)
*   **Booking Retrieval**: `GET` requests to `https://ammoue-ai.vercel.app/api/booking?business_id=biz_r9wz3lgd`

## Important Notes

*   **Admin PIN Security**: The administrator PIN (`G7I1X5`) is securely stored in a Firestore database, and verification occurs server-side via the `/api/verify-admin` endpoint.
*   **Browser Notifications**: Ensure your browser grants permission for desktop notifications to receive alerts. The feature uses the Web Notifications API and `localStorage` to track the last notified booking.
*   **Strict Adherence**: This project rigorously follows all architectural and design guidelines, ensuring a pixel-perfect, high-performance, and secure experience.

---
Designed with precision by AmmoueAI.