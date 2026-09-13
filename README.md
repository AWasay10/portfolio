# AW Services Website

A static portfolio site with a working contact form, backed by a small
serverless function (`api/contact.js`) that emails submissions to
awasay1012@gmail.com.

## Deploy for free on Vercel

1. Create a free GitHub account (if you don't have one) and a free Vercel
   account at vercel.com, signing in with GitHub.
2. Create a new GitHub repository and upload these three items exactly as
   they are: `index.html`, the `api` folder (with `contact.js` inside), and
   `package.json`.
3. In Vercel, click "Add New Project" and import that GitHub repository.
   Leave the default settings — Vercel auto-detects the `api` folder as
   serverless functions and serves `index.html` as the site.
4. Before deploying, generate a Gmail App Password: go to
   myaccount.google.com/apppasswords (requires 2-Step Verification turned on
   for the Gmail account), create one for "Mail", and copy the 16-character
   code.
5. In the Vercel project, go to Settings > Environment Variables and add:
   - `GMAIL_USER` = awasay1012@gmail.com
   - `GMAIL_APP_PASSWORD` = the 16-character app password from step 4
6. Click Deploy. Vercel gives you a free URL like
   `aw-services.vercel.app`.
7. Test the contact form on the live site — a submission should arrive in
   awasay1012@gmail.com within a few seconds.

You can later connect a custom domain from Vercel's project settings, still
on the free plan.
