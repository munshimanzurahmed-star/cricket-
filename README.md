# IPL Cricket Event Website

A responsive IPL-inspired event website built with React, Vite and Node.js/Express.

## Features
- Responsive home page with featured match and countdown
- 10 editable demo team profiles
- Match schedule with team filter
- Ticket booking form with unique booking reference
- Demo QR-style ticket (the booking reference is encoded as a QR code)
- Live-score screen clearly labelled as demo data
- Stadium information and FAQs
- Simple admin dashboard showing bookings and sales
- Node.js API with JSON-file persistence for a zero-database local demo

> This is an independent student project, not the official IPL website. Team names are used as illustrative sports data. The match schedule, scores, ticket prices and booking information are demonstration data, not official or live information.

## Requirements
- Node.js 18 or newer
- npm

## Run locally

From this project folder:

```bash
npm run install:all
npm run dev
```

Open the Vite URL shown in the terminal (usually http://localhost:5173).
The API runs at http://localhost:4000.

## Production build

```bash
npm run build
npm start
```

The Express server serves the API. To host the frontend separately, deploy the `client/dist` folder to a static host and set `VITE_API_URL` to your deployed API URL before building.

## Data storage
The backend saves bookings in `server/data/bookings.json`. This is convenient for a local demo, but it is not a production database. For a deployed multi-user application, replace this with Supabase/PostgreSQL and use proper authentication and server-side seat inventory.

## Admin demo
Open the Admin tab in the website. This sample admin view is intentionally a classroom prototype and is not protected by authentication. Do not use it to manage real customer information.

## Before real-world use
- Connect a verified cricket data provider for real scores and schedules.
- Connect a payment provider (for example, a supported payment gateway) and verify payments server-side.
- Add authentication and role-based access for admin users.
- Use a real database and transactional seat reservation to prevent double booking.
- Add privacy, refund, cancellation and event terms.
- Obtain permission for any official logos, team assets or trademarks.
