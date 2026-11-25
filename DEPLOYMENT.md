# GS Digital Studio — Deployment Runbook

## Source of truth

- GitHub: https://github.com/gsalviatti/gs-digital-studio
- Website: `index.html` (single-file Bootstrap with inline CSS and JS)
- Formspree: `https://formspree.io/f/mdegblpa`
- Business inbox: contactgsdigitalstudio@gmail.com

## Current Cloudflare hosting

- Worker script: `gs-digital-studio`
- Account workers.dev subdomain: `gsalviatti-studio`
- Expected URL: https://gs-digital-studio.gsalviatti-studio.workers.dev/
- First API deployment 2026-11-25, version `e05056aa-a487-42de-9a45-6c05af186a04`
- Cloudflare API reported 100% traffic to that version and script subdomain enabled.
- External HTTP/browser verification was not possible from the assistant's environment at deployment time. Verify the URL manually.

## GitHub / Cloudflare synchronization

**Important:** Git-based continuous deployment is **not configured**. The attempt to attach the GitHub repository to Cloudflare Pages failed due to a Cloudflare Pages Git installation error (8000011). The current Worker contains a copy of the HTML from GitHub embedded in the Worker script. Future pushes to GitHub **will not update Cloudflare automatically**.

For later updates, either:
1. Repair the Cloudflare Pages GitHub installation and move to an automated Git deploy, **or**
2. Redeploy the updated HTML into the Worker from this repository. Do not assume changes are live until Cloudflare confirms deployment and the public URL is retested.

## Production verification checklist

- [ ] Public HTTPS URL loads and displays GS Digital Studio
- [ ] EN and PT navigation/labels/pricing work
- [ ] Mobile view works, no horizontal overflow
- [ ] Visto Certo, Following Gabi and professional portfolio links open
- [ ] Formspree test inquiry submits successfully on the hosted domain
- [ ] New inquiry appears in Formspree Submissions
- [ ] Email notification arrives in the studio Gmail inbox
- [ ] Privacy notice and consent wording reviewed before public marketing
- [ ] Formspree domain restrictions, if enabled, allow the production domain

## Security

Never commit customer inquiries, passwords, tokens or private information to this public repository. Provider access and billing must remain with the owner.
