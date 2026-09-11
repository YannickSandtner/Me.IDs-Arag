# Intellectual Twin in Insurance — ARAG

Bilingual (EN/DE) Eraneos landing page about demographic change, leadership and knowledge retention, prepared as an approach to target client ARAG.

Live / canonical URL: <https://orange-ground-08ca4a703.5.azurestaticapps.net/>

GitHub Pages fallback: <https://florianliepe.github.io/Me.IDs-Arag/>

## Positioning

The four insurance use cases (succession, medical risk assessment expertise, benefits assessment and leadership knowledge) are explicitly labelled proposals and hypotheses to validate. The two specialist use cases focus on private health insurance, with decisions retained by authorised people. This is not an existing engagement, endorsement, joint initiative or case study. No claims about ARAG's internal staffing, processes or performance are made.

Private-health-insurance copy was supplied and approved by the user, with a corresponding English translation. Logos and Dr. Oliver Hüfner's portrait were supplied and approved by the user. Eraneos styling and the existing page structure were preserved; the four use cases use the same card design in a two-column desktop grid.

## Isolation and deployment

Cloned from the existing insurance landing page into `florianliepe/Me.IDs-Arag`. Only the ARAG repository and its dedicated Azure Static Web App are modified and published; the source site remains untouched.

GitHub Pages deploys from `main` through `.github/workflows/pages.yml`. The dedicated Azure deployment uses `.github/workflows/azure-static-web-apps.yml` and the repository secret `AZURE_STATIC_WEB_APPS_API_TOKEN_ARAG`. It targets only `intellectual-twin-insurance-arag` at <https://orange-ground-08ca4a703.5.azurestaticapps.net/> in resource group `rg-ai-intellectual-twin`. Only public site files and the Azure configuration are staged; source documentation and tests are not published.

## Contact form

- Service: FormSubmit; main recipient `florian.liepe@eraneos.com`
- Hidden CC recipients: Dr. Oliver Hüfner, `Oliver.Huefner@eraneos.com`, and Nicolas Faulbecker, `Nicolas.Faulbecker@eraneos.com`
- Displayed team: Dr. Florian Liepe, Dr. Oliver Hüfner (Partner · Eraneos), and Nicolas Faulbecker (Director Insurance)
- Required name, company, business email, topic, message and consent
- No confidential, policyholder or sensitive data should be submitted
- Success redirect uses the active origin and directory, preserving the GitHub Pages repository path
- First live submission may require recipient activation; delivery and mailbox receipt require a separately authorised live test

## Domain

The Azure-generated hostname is the initial canonical address. Canonical/social URLs, the form return URL and QR code target it. GitHub Pages remains available as a fallback. A custom domain can be attached later without affecting the original insurance site.

## Validation

Run `node tests/validate.cjs`. It checks translated copy, ARAG positioning, contact settings, local assets, source isolation and language/form behavior for GitHub Pages, Azure and disabled browser storage. QR decoding is verified separately against the canonical Azure URL.
