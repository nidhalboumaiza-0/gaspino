# Gaspino

Full-stack mobile application designed to reduce food waste by helping users discover nearby products and offers. The Flutter client communicates with a Node.js API and uses location-aware product search.

## Features

- Browse products available within a selected distance
- Search products by name
- User authentication and profile management
- Location-aware discovery
- Product and notification workflows

## Architecture

```text
client/  Flutter application using BLoC and clean architecture concepts
server/  Express and MongoDB REST API
```

## Run Locally

1. Install Node.js 18 or newer, Flutter, and MongoDB. Start MongoDB locally or prepare a MongoDB Atlas connection.
2. Open a terminal in `server/` and install the API dependencies:

   ```bash
   cd server
   npm install
   ```

3. Create `server/.env` with the API configuration:

   ```dotenv
   NODE_ENV=development
   PORT=3000
   DATABASE=mongodb://127.0.0.1:27017/gaspino
   JWT_SECRET=replace-with-a-long-random-value
   JWT_EXPIRE_IN=1d
   REFRESH_TOKEN_SECRET=replace-with-another-long-random-value
   REFRESH_TOKEN_EXPIRE_IN=30d
   EmailMailer=your-smtp-host
   PORTMAILER=587
   USERMAILER=your-development-email
   PASSWORDMAILER=your-email-app-password
   ```

4. Start the backend:

   ```bash
   npm start
   ```

5. In `client/.env`, set `URL` to the API prefix and `URLIMAGE` to the server's image URL. For an Android emulator, use values such as:

   ```dotenv
   URL=http://10.0.2.2:3000/api/v1
   URLIMAGE=http://10.0.2.2:3000/images/
   ```

   Use `localhost` for a desktop client or the computer's LAN IP for a physical phone.

6. Open another terminal and install the Flutter dependencies:

   ```bash
   cd client
   flutter pub get
   flutter devices
   ```

7. Run the application:

   ```bash
   flutter run
   ```

Keep development credentials local and never commit production secrets.
