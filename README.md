# CHINARLI.ONLINE — Website starter

An English-only, responsive static website starter for the Arli village community.

## Files
- `index.html` — page structure and content
- `style.css` — responsive visual design
- `script.js` — navigation and sign-in modal interactions
- `assets/favicon.svg` — site icon

## Preview locally
Open `index.html` in a web browser. For a more realistic local preview, use the Live Server extension in Visual Studio Code.

## Publish with GitHub Pages
1. Create or open your GitHub repository.
2. Upload all files and folders from this package. `index.html` must be in the repository's root.
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Choose the `main` branch and `/ (root)`, then save.
6. Wait for the Pages deployment to finish.

## Custom domain
In **Settings → Pages**, enter `chinarli.online` in the Custom domain field and save. Configure the DNS records at the company where the domain's DNS is managed, following GitHub's current documentation:
https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site

Do not delete or replace existing DNS records until you know what they are used for. Enable **Enforce HTTPS** after GitHub confirms the domain is configured.

## Important: backend features are not connected yet
This is a front-end starter. It does **not** currently provide working accounts, Google/Facebook OAuth, email or SMS OTP, two-step verification, a database, public community posting, or real-time chat. The sign-in buttons are intentionally disabled so visitors are not misled into thinking authentication is secure or active.

Those features need a backend service such as Supabase, provider configuration, database tables, security rules, and deployment-specific environment configuration. Never put secret API keys or service-role keys in frontend JavaScript. Do not collect real passwords or OTPs until secure authentication is configured.

## Before launch
- Confirm the village information and map pin are correct.
- Add only photos you have permission to publish.
- Add a privacy policy, terms, community guidelines, and a way to contact the site administrator before enabling accounts or user-generated content.
- Have an adult/trusted site administrator moderate posts and chat, and avoid publishing residents' private contact details without consent.
