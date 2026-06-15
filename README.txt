NEXORA NETLIFY FORM — DEPLOY INSTRUCTIONS

Files in this package:
- index.html
- netlify.toml

Correct Netlify settings:
- Branch: main
- Base directory: leave empty
- Build command: leave empty
- Publish directory: .
- Functions directory: leave default

Important:
1. Put index.html and netlify.toml in the ROOT of your GitHub repo.
2. Redeploy the site.
3. In Netlify, go to Forms and make sure form detection is enabled.
4. After redeploy, the form should appear as: photography-brand-intake
5. Test using the live *.netlify.app link, not a local file.

Why this version is fixed:
- No FormSubmit.
- No Google permission needed.
- No JavaScript preventDefault blocking the submission.
- No broken /thank-you.html action path.
- Uses a normal Netlify HTML POST form.
- Splits photo upload into 5 separate fields because Netlify only supports one file per upload field.
- Total form submission with files must stay under Netlify’s 8MB limit.
