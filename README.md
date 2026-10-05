# Farhan Rafi Telecom
Android-ready recharge app + Node.js backend + PostgreSQL + bKash/recharge API integration points.

## Included
- Customer registration/login with JWT
- Wallet balance and transaction ledger
- Mobile recharge order flow
- Recharge history
- Admin endpoints for users, orders and wallet adjustments
- bKash payment adapter placeholder
- Recharge-provider adapter placeholder
- Prisma/PostgreSQL schema
- Flutter Android app starter UI

## Important
Real bKash and recharge-provider credentials are intentionally NOT included. Put them in `backend/.env` after receiving credentials from your provider.

## Backend
```bash
cd backend
npm install
cp .env.example .env
npx prisma generate
npx prisma migrate dev --name init
npm run dev
```

## Flutter app
Install Flutter, then:
```bash
cd app
flutter pub get
flutter run
```
Set `API_BASE_URL` in `lib/config.dart` to your deployed backend URL.

## Default admin setup
After migration, run:
```bash
npm run seed
```
The seed creates an admin using the credentials in `.env`.

## Production checklist
- Use HTTPS
- Replace JWT secret
- Configure PostgreSQL
- Add real bKash credentials and callback URL
- Add real recharge API credentials/provider mapping
- Configure Android app signing
- Set proper business/legal information and transaction limits
