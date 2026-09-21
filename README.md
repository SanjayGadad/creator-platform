# CreatorX — full MVP except payment integration

## What is included
- Responsive web UI
- Creator onboarding and authentication
- Brand onboarding/authentication
- SQLite database
- JWT authentication
- Creator profiles and search
- Campaign creation
- Campaign marketplace
- Creator campaign applications
- Match-scoring endpoint for campaign/creator matching
- Campaign analytics
- Attribution event API
- Production-ready extension points for a payment provider

## Run
1. Install Node.js 18+.
2. `cd backend`
3. `npm install`
4. Copy `.env.example` to `.env` and change JWT_SECRET.
5. `npm start`
6. Open http://localhost:4000

## Payment deliberately excluded
There is no payment gateway code, checkout, payment secret, or payout implementation.

When ready, add payment after campaign creation using:
- server-side order creation
- provider checkout on the client
- server-side signature verification
- webhook verification
- database payment state
- payout/KYC workflow

Do not store card numbers or CVV. Do not trust client-side payment success.

## Production upgrades recommended
- PostgreSQL instead of SQLite
- Redis/job queue
- object storage for portfolios
- social OAuth/API integrations
- stronger RBAC
- audit logs
- rate limiting
- CSRF protection where applicable
- encrypted sensitive payout/KYC fields
- verified social metrics
- attribution deduplication and fraud detection
- real ML model after enough campaign data
