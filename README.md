# Region 3 Maintenance — Dashboard + Fleet Only

No login, no passwords, no database dependency. Only Dashboard and Fleet Maintenance tabs.

## Install
Upload the contents of this ZIP to the ROOT of your GitHub repository, preserving the `public` folder. Do not upload an extra enclosing folder. The root must contain `server.js`, `package.json`, and `public/`. Remove old root-level `index.html` and `app.js` if present. Railway runs `npm start`.

## Persistent storage
Set Railway `DATA_DIR=/app/data` and attach a persistent volume mounted at `/app/data`. Without it, data may be lost when redeploying. Existing compatible `records.json` data is preserved.

## Test
Open `/api/data` on your deployed domain: it should return JSON with vehicles. Dashboard and Fleet Maintenance should load without a login.

## Access warning
This public site has NO LOGIN, as requested. Anyone who knows its address can change fleet records. Do not store confidential information.
