# FoodTrace ERP — Cloud-based Food Manufacturing ERP & Traceability Platform

Track ingredient lots, production batches, QC and shipments, and trace any lot or batch forward and backward for recalls.

## Run locally
```bash
npm install
npm start   # http://localhost:3000
```

## Deploy on Render
1. Push this repo to GitHub.
2. In Render: **New → Blueprint** (uses `render.yaml`), or **New → Web Service** with build `npm install` and start `npm start`.
3. Open the Render URL.

## Notes
- Data is in memory and resets on restart. Replace the `db` object in `server.js` with PostgreSQL (Render offers a free instance) for persistence.
- Rules enforced: only Released lots go into batches, only QC-passed batches ship, stock is deducted on batch creation.
