# Ten — Long/Short Portfolio Backtesting (Visual Redesign)

This repository contains a visual refresh of the original Ten long/short portfolio backtesting app.

## What changed
- Updated visual styling, spacing, responsive presentation, card surfaces, controls, tables, and theme colors.
- Preserved the existing single-file application structure and JavaScript logic. This redesign intentionally changes CSS presentation only.

## App
Open `index.html` directly or deploy this repository as a static site on Netlify. No build command is required.

## Saving your data
By default the page saves to the browser you use. To save to an account instead (so it works across devices and survives clearing site data), connect a free Supabase project:

1. Create a project at supabase.com.
2. Open **SQL Editor**, paste the contents of `supabase-setup.sql`, and run it.
3. In **Authentication -> Providers -> Email**, keep email sign-in on. For the simplest sign-up, turn off "Confirm email".
4. In **Project Settings -> API**, copy the **Project URL** and the **anon public key**.
5. In `index.html`, find `var SUPABASE_URL = "", SUPABASE_ANON_KEY = "";` and put the two values between the quotes. The anon key is meant to be public: the database rules in step 2 make each user's data readable only by that user.
6. Commit. The page now asks you to sign in and saves your portfolio to your account.

Never put the `service_role` key in this file.

The original repository and deployment are separate and have not been changed by this redesign.
