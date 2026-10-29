# BHUMI-AI

BHUMI-AI is a static land-record review frontend backed by the Node/Express and MongoDB API in [`server/`](./server/).

## Run the backend locally

From the `server` directory:

```powershell
npm install
Copy-Item .env.example .env
npm run check:db
npm run dev
```

Set `MONGODB_URI` and `MONGODB_DB` in `.env` to a local MongoDB or MongoDB Atlas connection. Never commit `.env` or credentials; `.env.example` contains placeholders only.

The API runs on `http://localhost:3000`. Serve the static frontend on `http://127.0.0.1:8080` (for example with the existing local static server) so its `/api` requests can be reverse-proxied to the backend, or configure the deployment proxy to route `/api` to port 3000.
