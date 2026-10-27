# ClinicFlow — Vercel-ready clickable demo

Independent illustrative concept for legal-aid clinic coordination. **Not an official GBLS service, not legal advice, and not suitable for real client information.** All names and legal-change triggers are illustrative.

## Local development

Requires Node.js 20+ and npm.

```bash
npm install
npm run dev
```

Open the local URL printed by Vite. `npm run build` creates the static `dist/` folder.

## Deploy to Vercel

1. Extract this archive and put the `clinicflow` folder in a GitHub repository (or use Vercel CLI from that folder).
2. In Vercel, choose **Add New → Project**, import the repository, and set **Root Directory** to `clinicflow` if the repository contains a parent folder.
3. Framework preset: **Vite**; Build command: `npm run build`; Output directory: `dist`; Install command: `npm install`.
4. No environment variables are needed. Click **Deploy**. Visit the generated URL and test the flows below.

CLI alternative: `npm install -g vercel`, `vercel login`, then run `vercel` in this directory; `vercel --prod` publishes after reviewing the settings. These commands require your own authorized Vercel account.

## Acceptance checks

- Switch role to Attorney; open Legal review and toggle a draft's demo approval.
- Launch a new clinic; confirm generated tasks appear on Planning board and a draft appears in Legal review.
- Sign up a fictional volunteer, book a fictional client alias, and update that alias in Day-of queue.
- Export the **fictional** queue CSV and verify it contains only the demo aliases.
- Check the mobile layout and refresh: session data should reset (by design).

## Architecture / limitations

Vite + React, CSS, lucide-react. The app uses local React state only. There is **no Supabase**, authentication, server-side authorization, persistence, email/SMS, external calendar, production AI, or live translations. The language dropdown is a UI preview. Do not enter confidential or real client data. A future production build needs a security/privacy review, Supabase Auth + enforced RLS, tenant isolation, server-side attorney approval gates, audit logging, consent/retention rules, accessibility and verified translations.
