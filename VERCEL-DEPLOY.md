# AUCTION — Vercel Frontend Connected to Render

Backend API: https://auction-backend-x97o.onrender.com

## Deploy
1. Upload/import this folder into Vercel.
2. Framework Preset: Other.
3. Build Command: leave empty.
4. Output Directory: leave empty / root.
5. Deploy.

## Important Render setting
In the Render backend service, set `FRONTEND_URL` to the exact Vercel production URL, for example:
`https://your-project.vercel.app`

If you later add a custom domain, update `FRONTEND_URL` to that exact origin too (comma-separated if your backend accepts more than one origin).

## Backend health check
Open:
`https://auction-backend-x97o.onrender.com/api/health`
It should return JSON containing `ok: true`.

## What is connected
- Registration: POST /api/auth/register
- Login: POST /api/auth/login
- Session: GET /api/auth/me
- Auctions: GET /api/auctions
- Create auction: POST /api/auctions
- Images: POST /api/upload
- Bids: POST /api/auctions/:id/bids
- Watchlist: POST /api/watchlist/:id
- My bids: GET /api/my-bids
- My auctions: GET /api/my-auctions
- Notifications: GET /api/notifications

Authentication uses the backend HTTP-only `auction_token` cookie. Do not put passwords or the cookie value in localStorage.
