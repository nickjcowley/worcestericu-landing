# GitHub Pages Setup for worcestericu.com

## Steps

### 1. Create a GitHub repository
- Go to github.com and create a new **public** repository
- Name it anything (e.g. `worcestericu-landing`)

### 2. Upload the files
Upload these two files to the repository root:
- `index.html`
- `CNAME`

You can drag and drop them into the GitHub web interface.

### 3. Enable GitHub Pages
- In the repository, go to **Settings → Pages**
- Under "Source", select **Deploy from a branch**
- Choose **main** branch, **/ (root)** folder
- Click Save

GitHub will show you a green banner with the Pages URL once it's live (takes ~1 minute).

### 4. Point your domain at GitHub Pages
In your domain registrar (wherever you bought worcestericu.com), update the DNS:

| Type  | Name | Value                  |
|-------|------|------------------------|
| A     | @    | 185.199.108.153        |
| A     | @    | 185.199.109.153        |
| A     | @    | 185.199.110.153        |
| A     | @    | 185.199.111.153        |
| CNAME | www  | YOUR-GITHUB-USERNAME.github.io |

DNS changes take up to 24 hours to propagate.

### 5. Enable HTTPS
Once the domain is verified in Settings → Pages, tick **Enforce HTTPS**.

---

## Updating the page
To swap in the real URLs later, open `index.html` and find these two placeholders:
- `SHAREPOINT_URL_HERE` — replace with your NHS SharePoint link
- `WIX_ARCHIVE_URL_HERE` — replace with your free Wix domain URL

Then re-upload the file to GitHub (or edit it directly in the GitHub web editor).
