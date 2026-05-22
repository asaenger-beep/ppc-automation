# ⚡ PPC Automation

Project hub for building automation into PI's PPC programs.

**Live site:** `https://YOUR_GITHUB_USERNAME.github.io/ppc-automation`

---

## Quick setup (one-time)

### 1. Create the GitHub repo

1. Go to [github.com/new](https://github.com/new)
2. Name it `ppc-automation`
3. Set visibility to **Private** (share access with your collaborator by email after)
4. Click **Create repository**

### 2. Upload these files

Drag and drop the contents of this folder into the repo, or use the GitHub Desktop app to sync.

### 3. Enable GitHub Pages

1. In the repo, go to **Settings → Pages**
2. Under **Source**, choose **Deploy from a branch**
3. Select branch: `main`, folder: `/ (root)`
4. Click **Save**

After ~60 seconds, your site will be live at:
`https://YOUR_GITHUB_USERNAME.github.io/ppc-automation`

### 4. Add your Google Drive link

Open `index.html` and replace both instances of:
```
GOOGLE_DRIVE_FOLDER_LINK_HERE
```
with the actual shared Google Drive folder URL.

Also replace `YOUR_GITHUB_USERNAME` with your actual GitHub username in the header, footer, and Resources section.

### 5. Invite your collaborator

In the repo → **Settings → Collaborators** → **Add people** → enter their GitHub username or email.

---

## How to add artifacts

When you create a new script, doc, report, or dashboard, add it to `index.html` following the template in the `<script>` comment block at the bottom of the file.

**Artifact card template:**
```html
<div class="artifact-grid">
  <a class="artifact-card" href="PATH_TO_FILE" target="_blank">
    <div class="artifact-card-top">
      <div class="artifact-name">Name of artifact</div>
      <div class="artifact-ext">.py</div>
    </div>
    <div class="artifact-desc">What it does — one or two sentences.</div>
    <div class="artifact-meta">
      <span class="tag green">ready</span>
      <span class="tag">phase 1</span>
      <span class="artifact-date">May 2026</span>
    </div>
  </a>
</div>
```

**Tag colors:** default (blue) · `green` · `amber` · `purple`

---

## Folder structure (suggested)

```
ppc-automation/
├── index.html          ← the mini-site (edit this to add artifacts)
├── README.md           ← this file
├── scripts/            ← Python / JS automation scripts
├── docs/               ← strategy docs, specs, briefs
├── reports/            ← CSVs, Excel exports, data snapshots
└── dashboards/         ← HTML dashboard artifacts
```

---

## Collaborator notes

Context docs from the external collaborator live in the shared Google Drive folder linked in the site header. Reference those for background, briefs, and raw data.
