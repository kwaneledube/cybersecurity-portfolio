# Portfolio site (portfolio.isizuluai.co.za)

Static site: no build step, no dependencies.

## Files
- index.html: home page (about, credentials, projects, learning, contact)
- writeups.html: weekly lab write-ups
- style.css: all styling
- vercel.json: security headers (CSP, HSTS, X-Frame-Options and more)

## Before you publish
Replace these in index.html:
- YOUR_EMAIL_HERE
- YOUR_GITHUB_USERNAME
- YOUR_LINKEDIN_HANDLE

## Deploy (free)
1. Create a GitHub repo called `cybersecurity-portfolio` and push these files.
2. In Vercel: Add New > Project > import the repo > Deploy (no settings needed).
3. In the project: Settings > Domains > add `portfolio.isizuluai.co.za`. Vercel shows a CNAME target.
4. In TrueHost client area > DNS Management for isizuluai.co.za, add:
   - Type: CNAME
   - Name: portfolio
   - Target: the value Vercel gave you
5. Wait for DNS to update, then click Refresh in Vercel. HTTPS is automatic.

## Check your security headers
After it is live, test the site at securityheaders.com and aim for an A grade.

## Adding a write-up each Saturday
Copy the `<div class="post">` block in writeups.html, put the newest on top, and push to GitHub. Vercel redeploys automatically.
