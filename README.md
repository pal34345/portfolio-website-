# Setting this up — from your Android phone, no computer needed

## 1. Create the repo
- Go to github.com (or open the GitHub app), sign in.
- Tap **+ → New repository**.
- Name it something like `portfolio` (this becomes part of your URL).
- Make it **Public**. Create it.

## 2. Upload these three files
- Open the repo → **Add file → Upload files**.
- Upload `index.html` and `projects.json` from this package to the **root** of the repo.
- Create a folder called `files` in the repo (upload any file into a new path like `files/placeholder.txt` and GitHub will create the folder), then upload your real PDFs/PPTs there (AlphaEvolve report, switchgear manuals, Lacanian Ethics deck, etc).

## 3. Turn on GitHub Pages
- In the repo, go to **Settings → Pages**.
- Under "Build and deployment," set Source to **Deploy from a branch**, branch `main`, folder `/ (root)`. Save.
- After a minute, your site is live at:
  `https://YOUR_GITHUB_USERNAME.github.io/portfolio/`
- This link is what you share with anyone — recruiters, LinkedIn, your resume.

## 4. Add or update projects (whenever you want)
- Open `projects.json` in the repo → tap the pencil (edit) icon.
- Copy an existing entry block and change the title, description, type, and file path.
- Supported `type` values: `pdf`, `pptx`, `docx`, `xlsx`, `image`, `figma`, `link`, or leave blank for a plain download link.
- Commit the change — the live site updates within a minute or two.

## 5. Turn on comments (Giscus — free, no server)
- Go to giscus.app, sign in with GitHub.
- Point it at your `portfolio` repo (you'll need to enable **Discussions** on the repo first: Settings → General → Features → tick Discussions).
- Giscus will generate a code snippet with your real `data-repo-id` and `data-category-id`.
- Open `index.html` in your repo, find the `<script src="https://giscus.app/client.js"...` block near the bottom, and replace the placeholder `data-repo`, `data-repo-id`, and `data-category-id` values with the real ones giscus gives you.
- Visitors will need a free GitHub account to comment — that's the trade-off for a genuinely free, no-server comment system. They cannot edit or delete your project entries either way; they can only comment.

## 6. Embedding a Figma project
- In Figma, open your file → **Share → Embed** → copy the embed link.
- In `projects.json`, set `"type": "figma"` and paste that embed URL as `"file"`.

## Why this is AI-readable
This site is plain static HTML with real server-delivered content — no login wall, no JavaScript-only storage layer standing between the content and a reader. Any AI browsing tool or search crawler that fetches the page can read the project titles and descriptions directly from `projects.json` and the rendered page.
