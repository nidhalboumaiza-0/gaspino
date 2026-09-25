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

## Getting Started

```bash
cd server
npm install
npm start
```

In another terminal:

```bash
cd client
flutter pub get
flutter run
```

Provide the server's database, JWT, mail, and runtime settings through local environment configuration. Set the client API endpoint for your emulator or physical device.
