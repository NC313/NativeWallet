# NativeWallet

NativeWallet is a simple, mobile-first personal finance application designed to help you track your income and expenses with ease. It features a React Native (Expo) frontend and a Node.js (Express) backend, providing a complete solution for managing personal transactions. This project is not my personal invention and can be found to duplicate yourself with a few of the simple technologies listed and commonly used assets if you just want to quickly put it together for your own practice!

## Features

- **User Authentication:** Secure sign-up and sign-in functionality powered by Clerk.
- **Financial Summary:** A clear dashboard displaying your current balance, total income, and total expenses.
- **Transaction History:** View a detailed, chronological list of all your past transactions.
- **Create & Delete:** Easily add new transactions with a title, amount, and category, and delete them as needed.
- **Cross-Platform:** Runs on iOS, Android, and web via the Expo framework.

## Technology Stack

### Frontend (Mobile)

- **Framework:** React Native with Expo
- **Navigation:** Expo Router
- **Authentication:** Clerk
- **Language:** JavaScript

### Backend

- **Framework:** Node.js with Express.js
- **Database:** PostgreSQL (designed for NeonDB serverless)
- **Rate Limiting:** Upstash Redis
- **Language:** JavaScript (ESM)

## Getting Started

Follow these instructions to get a local copy of the project up and running for development and testing.

### Prerequisites

- [Node.js](https://nodejs.org/) (v18 or newer recommended)
- [npm](https://www.npmjs.com/)
- [Expo Go](https://expo.dev/go) app on your iOS or Android device for mobile testing.

### Backend Setup

1.  **Navigate to the backend directory:**
    ```sh
    cd backend
    ```

2.  **Install dependencies:**
    ```sh
    npm install
    ```

3.  **Set up environment variables:**
    Create a file named `.env` in the `backend` directory and add the following variables. These are required to connect to your database and rate limiter.

    ```env
    # Your PostgreSQL connection string (e.g., from NeonDB)
    DATABASE_URL="your_database_connection_string"

    # Your Upstash Redis credentials for rate limiting
    UPSTASH_REDIS_REST_URL="your_upstash_redis_url"
    UPSTASH_REDIS_REST_TOKEN="your_upstash_redis_token"

    # Optional: The port the server will run on (defaults to 5001)
    PORT=5001
    ```

4.  **Start the development server:**
    ```sh
    npm run dev
    ```
    The backend server will start, typically on port 5001.

### Mobile App Setup

1.  **Navigate to the mobile directory:**
    ```sh
    cd mobile
    ```

2.  **Install dependencies:**
    ```sh
    npm install
    ```

3.  **Start the Expo development server:**
    ```sh
    npx expo start
    ```

4.  **Run the app:**
    - A new browser tab will open with the Metro Bundler interface.
    - Scan the QR code using the Expo Go app on your mobile phone.
    - Alternatively, you can run directly in a simulator by pressing `i` for iOS or `a` for Android in the terminal where Expo is running.

---


