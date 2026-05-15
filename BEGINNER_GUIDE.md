# Chandan Kumar — Portfolio Site: Beginner's Complete Guide

This guide covers everything from creating your GitHub account to editing your
site content in five minutes, using only your web browser.

---

## What You'll Have When You're Done

A live website at:

```
https://YOUR-GITHUB-USERNAME.github.io/
```

Every time you edit a file on GitHub and click "Commit changes," your site
rebuilds automatically within about 60–90 seconds.

---

## Overview of the Files

```
chandan-portfolio/
├── config.yaml                  ← ALL YOUR CONTENT LIVES HERE
├── .github/
│   └── workflows/
│       └── hugo.yml             ← Auto-deploy script (do not edit)
├── static/
│   ├── Chandan_Kumar_Resume.pdf ← Upload your resume PDF here
│   └── images/
│       ├── hero.jpg             ← Upload your profile photo here
│       ├── engagements/         ← Upload case study images here
│       └── achievements/        ← Upload achievement images here
├── content/                     ← Leave empty for now (blog posts go here later)
└── .gitignore                   ← Tells GitHub what files to ignore (do not edit)
```

**Your rule of thumb:**
- For content changes (text, jobs, skills): edit `config.yaml`
- For adding files (photo, PDF): upload to the `static/` folder
- Everything else: leave alone

---

## PART 1: Create Your GitHub Account

*Time: about 5 minutes. Do this first.*

1. Open your web browser and go to **https://github.com**

2. Click the **"Sign up"** button (top right).

3. Enter these details:
   - **Email:** `chandan.im.official@gmail.com`
   - **Password:** choose something strong (you'll need it to log in)
   - **Username:** This becomes part of your website URL, so choose carefully.
     - It cannot contain dots — so `chandan.im.official` won't work.
     - Good options: `chandankumar`, `chandan-kumar`, `chandanimofficial`
     - Whatever you pick, your site URL will be: `https://YOURUSERNAME.github.io/`
     - You can check availability as you type — a green tick means it's free.

4. Complete the verification puzzle and click **"Create account"**.

5. Check your email (`chandan.im.official@gmail.com`) for a verification code
   and enter it on GitHub.

6. When asked about your plan, choose **"Free"** — it has everything you need.

**Write down your chosen username here:** ____________________________

---

## PART 2: Create the Repository

*A "repository" (or "repo") is just a folder that GitHub hosts for you.*

**This step is critical: the repo name must follow an exact format.**

1. After logging in to GitHub, click the **"+"** icon (top right) and select
   **"New repository"**.

2. Fill in the form exactly like this:
   - **Repository name:** `YOUR-USERNAME.github.io`
     - Example: if your username is `chandankumar`, type: `chandankumar.github.io`
     - This exact format is what activates the free GitHub Pages hosting.
   - **Description:** `My professional portfolio website` (optional, but helpful)
   - **Public / Private:** Select **"Public"**
     - (GitHub Pages on free accounts requires the repo to be public)
   - **Add a README file:** Leave this **unchecked** — we'll upload our own files.

3. Click **"Create repository"**.

4. You'll see an empty repo page. Keep this browser tab open — you'll need it
   in the next step.

---

## PART 3: Update config.yaml With Your GitHub Username

Before uploading, you need to set your GitHub username in one place:

1. On your computer, find the file: `chandan-portfolio/config.yaml`
2. Open it in Notepad (right-click the file → "Open with" → Notepad)
3. Near the top, find this line:
   ```
   baseURL: "https://YOUR-GITHUB-USERNAME.github.io/"
   ```
4. Replace `YOUR-GITHUB-USERNAME` with your actual GitHub username.
   Example: `baseURL: "https://chandankumar.github.io/"`
5. Save the file (Ctrl+S).

---

## PART 4: Upload Your Files to GitHub

*There are two methods. Use Method A (GitHub Desktop) if you prefer clicking
buttons. Use Method B (web upload) if you want to stay in the browser.*

---

### Method A — GitHub Desktop App (Recommended for beginners)

GitHub Desktop is a free app that handles all the technical Git commands
with a simple interface.

1. **Download GitHub Desktop** from: https://desktop.github.com/
   Install it and sign in with your GitHub account.

2. Click **"Clone a repository"** — then click **"Add"** → **"Create new repo"**
   — actually, since the repo exists on GitHub already, click:
   **File → Clone Repository → URL**
   Enter: `https://github.com/YOUR-USERNAME/YOUR-USERNAME.github.io`
   Choose a folder on your computer to save it to. Click **"Clone"**.

3. Open File Explorer. Navigate to the folder you just cloned.
   Copy ALL files from your `chandan-portfolio/` folder into this cloned folder.
   (Drag and drop, or Ctrl+A, Ctrl+C, then Ctrl+V in the cloned folder.)

4. Go back to GitHub Desktop. You'll see a list of "Changes" on the left — these
   are the files you just added.

5. At the bottom left, type a summary like: `Initial site setup`
   Then click **"Commit to main"**.

6. Click **"Push origin"** (top right). Your files are now on GitHub!

---

### Method B — Upload via GitHub Website (No app required)

*This works for the initial upload. For future edits, the web editor is easier.*

1. Go to your empty repository on GitHub.

2. Click **"uploading an existing file"** (shown as a link on the empty repo page).
   If you don't see that link, click **"Add file"** → **"Upload files"**.

3. **IMPORTANT:** You need to upload the files in the correct folder structure.
   GitHub's web uploader supports drag-and-drop, including folders.

   Drag the entire `chandan-portfolio/` folder contents into the upload area.
   You should see all the files and folders appear.

4. Scroll down. In the "Commit changes" section, type:
   `Initial site setup`

5. Click **"Commit changes"**.

**Note:** The web uploader sometimes struggles with deeply nested folders like
`.github/workflows/`. If that folder doesn't upload correctly:
- After uploading the main files, click "Add file" → "Create new file"
- In the filename box, type: `.github/workflows/hugo.yml`
  (GitHub auto-creates the folders as you type the slashes)
- Copy and paste the contents of your local `hugo.yml` file into the text editor
- Click "Commit new file"

---

## PART 5: Enable GitHub Pages

*One-time setup — takes about 2 minutes.*

1. In your GitHub repository, click the **"Settings"** tab (top menu).

2. In the left sidebar, scroll down and click **"Pages"**.

3. Under **"Source"**, click the dropdown and select **"GitHub Actions"**.
   (Not "Deploy from a branch" — choose "GitHub Actions".)

4. Click **"Save"** if a save button appears.

5. Now go to the **"Actions"** tab of your repo. You should see a workflow
   running (orange/yellow dot = in progress, green = done, red = error).

6. Wait about 60–90 seconds, then refresh the page. When you see a green
   checkmark, your site is live!

7. Go to: `https://YOUR-USERNAME.github.io/`

   Your site should be visible. If it shows a 404, wait another minute and
   refresh — first deployments sometimes take a little longer.

---

## PART 6: Add Your Profile Photo and Resume

### Adding Your Profile Photo

1. Find a professional headshot photo on your computer.
   - Best format: JPEG (.jpg)
   - Recommended size: 400×400 pixels (square) or 400×500 pixels (portrait)
   - Professional background, business attire — think LinkedIn profile photo

2. Rename the file to: `hero.jpg`

3. Go to your GitHub repository.

4. Click into the `static` → `images` folder.

5. Click **"Add file"** → **"Upload files"**.

6. Drag your `hero.jpg` into the upload area.

7. Click **"Commit changes"** (add a note like `Add profile photo`).

Your photo will appear on the site after the next build (about 60 seconds).

### Adding Your Resume PDF

1. Prepare your resume as a PDF file.

2. Rename it to: `Chandan_Kumar_Resume.pdf`
   (The filename must match exactly what's in config.yaml under `button.url`)

3. Go to your GitHub repository, click into the `static` folder.

4. Click **"Add file"** → **"Upload files"**, drag your PDF in.

5. Click **"Commit changes"**.

Visitors will now be able to download your resume from the site.

---

## PART 7: Editing Your Content

*This is how you'll maintain the site day-to-day — all edits happen in your
browser on GitHub.*

### How to Open and Edit config.yaml

1. Go to your repository on GitHub.

2. Click on **`config.yaml`** in the file list.

3. Click the **pencil icon** (Edit this file) at the top right of the file view.

4. The file opens in a text editor directly in your browser.

5. Find the section you want to change (use Ctrl+F to search).

6. Make your edits.

7. Scroll to the bottom. Under **"Commit changes"**, type a short note
   describing what you changed (e.g., `Update job title at Firm X`).

8. Click **"Commit changes"** (the green button).

Your site will rebuild automatically. Check the **"Actions"** tab to watch the
progress — green tick means it's live.

---

### How to Update Your Job Title or Headline

Search for `subtitle:` in config.yaml:

```yaml
    subtitle: "Strategy & Operations Consultant"
```

Change the text between the quotes. Commit.

---

### How to Add a New Job

In config.yaml, find the `experience:` section. Look for a block like this:

```yaml
      - job: "Senior Consultant — Strategy & Operations"
        company: "Global Management Consulting Firm"
        companyUrl: ""
        date: "Mar 2021 – Present"
        featuredLink:
          enable: false
        info:
          enable: true
          content: "Full-time | London, UK"
        content: |-
          Your job description here.

          - Bullet point one
          - Bullet point two
```

**To add a new job:**
1. Copy the entire block above (from `      - job:` to the blank line)
2. Paste it *above* the existing first job (so newest is always first)
3. Fill in your new job's details
4. Commit changes

**Important:** Keep the indentation (the leading spaces) exactly the same.
YAML breaks if you change the spacing.

---

### How to Add a New Case Study / Engagement Card

In config.yaml, find the `projects:` section. Copy one `      - title:` block
and paste it, then fill in your new engagement:

```yaml
      - title: "Your Engagement Title"
        content: >
          2–3 sentences describing the engagement and its outcome.
          Keep quantified results (%, £, timeframes) where possible.
        image: /images/engagements/your-image.jpg
        featured:
          name: "View Details"
          link: "#"
        badges:
          - "Tag One"
          - "Tag Two"
          - "Tag Three"
```

If you don't have an image, simply remove the `image:` line entirely.

---

### How to Add a New Certification or Degree

In config.yaml, find the `education:` section. Copy one entry block and paste:

```yaml
      - title: "Your Certification Name"
        school:
          name: "Issuing Organisation"
          url: "https://organisationwebsite.com"
        date: "2024"
        content: |-
          One sentence about what this certification covers.
```

---

### How to Add a New Achievement

In config.yaml, find the `achievements:` section. Copy one entry block:

```yaml
      - title: "Your Award or Achievement"
        content: >
          One or two sentences describing it — include the year
          and why it was awarded if possible.
        url: ""
```

---

### How to Update Your LinkedIn URL

Search for `linkedin.com/in/` in config.yaml. It appears in two places:
1. In the `socialLinks` section under `hero:`
2. In the `footer:` section under `socialNetworks:`

Update both lines to match your profile URL.

---

### How to Add an Image to a Case Study Card

1. Prepare an image (any JPEG/PNG; 800×500 pixels recommended)
2. Go to GitHub → `static` → `images` → `engagements` folder
3. Click **"Add file"** → **"Upload files"**, upload your image
4. In config.yaml, update the `image:` line for that engagement:
   ```yaml
   image: /images/engagements/your-filename.jpg
   ```
5. Commit both changes

---

## PART 8: Previewing Changes Before They Go Live

**Option A — View the Actions build log**

After committing, go to the **"Actions"** tab. Click the latest workflow run.
You can see build output and any errors here.

**Option B — Preview locally (advanced)**

If you've installed Hugo on your computer (see https://gohugo.io/installation/),
you can run `hugo server` in the project folder and preview at
`http://localhost:1313` before committing to GitHub.

---

## PART 9: Adding a Custom Domain (Optional, Future)

If you later want to use `www.chandankumar.com` instead of the GitHub.io URL:

1. Buy a domain from any registrar (Namecheap, GoDaddy, Google Domains, etc.)

2. In your domain registrar's DNS settings, add a CNAME record:
   - **Name/Host:** `www`
   - **Value:** `YOUR-USERNAME.github.io`

3. In your GitHub repo, go to **Settings → Pages → Custom domain**
   Type your domain (`www.chandankumar.com`) and click Save.

4. Create a file called `CNAME` in your repo's root with one line:
   `www.chandankumar.com`

5. Wait up to 24 hours for DNS to propagate. GitHub will also auto-enable HTTPS.

---

## PART 10: Setting Up the Formspree Contact Form (Optional)

By default, the "Contact Me" button opens your email client. If you want visitors
to fill out a form on the site instead:

1. Go to **https://formspree.io** and sign up (free, no credit card)

2. Click **"+ New Form"**, give it a name like "Portfolio Contact"

3. Copy the form ID shown in the URL (looks like `abcdefgh`)

4. In `config.yaml`, find the `formspree:` section and update:
   ```yaml
   formspree:
     enable: true           # Change false to true
     formId: "abcdefgh"     # Replace with your actual form ID
   ```

5. Commit. Formspree will email you whenever someone fills out the form.

---

## Troubleshooting

### "The site didn't update after I committed"

1. Go to the **"Actions"** tab in your repository.
2. If you see an orange dot: the build is still running. Wait 60–90 seconds.
3. If you see a red X: click on the failed run to see the error message.
   The most common cause is a YAML formatting error in `config.yaml`
   (usually a wrong indent or a missing quote).

### "I got a red X / build failed — YAML error"

YAML is sensitive to indentation. Common mistakes:
- Using **tabs** instead of spaces (use the spacebar, not the Tab key)
- A missing closing quote `"`
- Text that's indented incorrectly

**How to fix:** Look at the error message in the Actions log — it tells you
which line number has the problem. Go to that line in config.yaml and check
the spacing and quotes match the surrounding lines.

### "My site shows a 404 error"

- Check that GitHub Pages is set to deploy via **"GitHub Actions"** (not a branch)
- Make sure the latest Actions run completed with a green tick
- Try visiting `https://YOUR-USERNAME.github.io/` (with the trailing slash)
- Wait 5 minutes and try again — DNS can be slow on first setup

### "My profile photo isn't showing"

- Make sure you uploaded it to `static/images/` (not just `static/`)
- The filename must be exactly `hero.jpg` (case-sensitive)
- Check that config.yaml has `image: /images/hero.jpg` (with the leading `/`)

### "The download resume button doesn't work"

- Upload your PDF to the `static/` folder (not a subfolder)
- Filename must be exactly `Chandan_Kumar_Resume.pdf`
- Check config.yaml has `url: "/Chandan_Kumar_Resume.pdf"` (note the leading `/`)

---

## Your Final Shareable URL

Once everything is set up, your site will be permanently available at:

```
https://YOUR-GITHUB-USERNAME.github.io/
```

Share this link in:
- Your LinkedIn "About" section (paste under "Website")
- Your email signature
- Job application forms
- Your CV as a "Portfolio" link

---

## Quick Reference Card

| What to do | Where |
|---|---|
| Edit text, jobs, bio | `config.yaml` → find the section, edit, commit |
| Add a new job | `config.yaml` → `experience:` → copy a block |
| Add a case study | `config.yaml` → `projects:` → copy a block |
| Add a certification | `config.yaml` → `education:` → copy a block |
| Add an achievement | `config.yaml` → `achievements:` → copy a block |
| Upload your photo | `static/images/hero.jpg` |
| Upload your resume | `static/Chandan_Kumar_Resume.pdf` |
| Check build status | Repository → "Actions" tab |
| View live site | `https://YOUR-USERNAME.github.io/` |
