# API endpoints
POST /api/auth/register
POST /api/auth/login
GET  /api/me
GET  /api/recharges
POST /api/recharges {operator,phone,amount}
POST /api/payments/bkash/create {amount}
GET  /api/admin/users (ADMIN)
POST /api/admin/wallet (ADMIN)
GET  /health

All protected endpoints use `Authorization: Bearer <JWT>`.
