# HiFarmers

Short repo README and developer quick-start for the `HiFarmers` monorepo (client + server).

**Project layout**
- `client/` — front-end app (React) with `src/`, `public/`, and UI components.
- `server/` — back-end API (Node/Express) with `controllers/`, `models/`, `routes/`, and `middleware/`.

Note: I observed some macOS resource-fork files in the repository (filenames starting with `._`). `.gitignore` has been added to ignore those and other dev artifacts.

Getting started (development)

1) Prerequisites
- Node.js (LTS recommended)
- npm (or yarn)

2) Install dependencies

PowerShell (from the repository root):

```
cd client
npm install

cd ../server
npm install
```

3) Run the apps (typical commands)

- Client (React):

```
cd client
npm start
```

- Server (Express):

```
cd server
npm start
```

If you use `nodemon` for automatic restarts during development, add a script in `server/package.json` such as:

```
"scripts": {
  "start": "node index.js",
  "dev": "nodemon index.js"
}
```

Environment variables

Create a `.env` file in `server/` with values required by your app. Typical variables for this kind of project may include:

- `MONGO_URI` or `DATABASE_URL` — MongoDB connection string
- `PORT` — Server port (e.g. `5000`)
- `JWT_SECRET` — Secret for signing JWTs
- `CLIENT_URL` — Frontend URL for CORS

Repository observations & next steps

- I inspected the `client/src` and `server/` directories. They contain React components and Express controllers respectively.
- I did not find usable `package.json` files at the top level of `client/` or `server/` in normal form; there are `._package.json` resource-fork artifacts present. Please verify that `client/package.json` and `server/package.json` exist and include the expected `scripts` and `dependencies`.
- If `package.json` files are missing, recreate them with `npm init -y` and add scripts like `start` and `dev` as described above.

How I can help next

- Create or repair `package.json` files for `client` and/or `server` with suggested scripts.
- Add a `Dockerfile` or `docker-compose.yml` for local dev.
- Wire up a sample `.env.example` with the expected keys.

If you want me to: tell me which of the above I should do next (repair package.json, create `.env.example`, add run scripts, or run tests). 
