**Hotel Booking App**

- **Simple React + Vite frontend** for browsing and managing hotel rooms. Includes a public booking UI and a protected owner dashboard.

**Quick Start**

- **Requirements:** Node 18+ and npm.
- **Install:** `npm install`
- **Run (dev):** `npm run dev`
- **Build:** `npm run build`
- **Preview:** `npm run preview`

**Login (admin)**

- Static admin email: `admin@admin.com` — use it on `/login` to access the owner dashboard.
- Auth is stored locally in `localStorage` (key: `hotel-booking-auth`). See `src/utils/auth.ts`.

**Main Routes**

- `/` — Home
- `/rooms` — All rooms
- `/rooms/:id` — Room details
- `/my-bookings` — User bookings
- `/login` — Admin login (static)
- `/owner` — Owner dashboard (protected)

**Tech & Structure**

- Framework: React + Vite
- Styling: Tailwind CSS
- Key folders:
	- `src/components` — UI components
	- `src/pages` — Page views (Home, AllRooms, Owner pages)
	- `src/utils` — small helpers (auth, constants)

**Notes for maintainers**

- Owner routes are guarded by `RequireAuth` (`src/components/RequireAuth.tsx`).
- The simple auth implementation is intended for local/demo use only. Replace with a proper auth provider for production.
- To change the admin email, update `ADMIN_EMAIL` in `src/utils/auth.ts`.

**Contributing**

- Open a PR on the `feature/login` branch or discuss changes via issues. Keep changes focused and small.

