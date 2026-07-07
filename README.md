# HFF Quiz, GitHub Pages setup

This folder is ready to publish as a free, live quiz page on GitHub Pages.

Files:
- `index.html` is the quiz (named index.html so the URL is clean)
- `images/hff-logo.png` is the logo in the top bar

---

## Part 1: Get it live (about 5 minutes)

You already have a GitHub account, so:

1. Go to **github.com** and click the **+** top right, then **New repository**.
2. Name it something like `hff-quiz`. Set it to **Public**. Click **Create repository**.
3. On the new repo page, click **uploading an existing file**.
4. Drag in **both** `index.html` and the whole `images` folder from this folder. Click **Commit changes**.
5. Go to **Settings** (top of the repo) then **Pages** (left menu).
6. Under **Branch**, choose **main**, keep the folder as **/ (root)**, and click **Save**.
7. Wait a minute or two, then refresh. GitHub shows your live link at the top, something like:
   `https://yourusername.github.io/hff-quiz/`

That link is your quiz. Share it, put it in your bio, run ads to it.

---

## Part 2: Make the email box actually collect emails

GitHub Pages only serves the page, it can't catch a form on its own. Easiest fix is a free service called **Formspree**.

1. Go to **formspree.io** and sign up (free plan is fine to start).
2. Create a new form. It gives you an endpoint that looks like `https://formspree.io/f/abcdwxyz`.
3. Open `index.html`, find `REPLACE_WITH_FORMSPREE_ENDPOINT`, and paste your endpoint in its place.
4. Re-upload `index.html` to your repo (same as Part 1, step 3 to 4).

Now every signup emails you, and it includes a field called **menopause_stage** with her quiz result, so you know exactly which stage she's in.

### Getting her into Flodesk with the right tag
Formspree collects the email, it doesn't push to Flodesk by itself. Two ways to close that loop:
- **Simple:** each signup lands in your inbox with her stage. Add her to Flodesk and tag her by stage. Fine for low volume.
- **Automatic:** connect Formspree to Flodesk with a Zapier zap (Formspree new submission → Flodesk add subscriber, using the menopause_stage field as the tag). Set it once, forget it.

If you'd rather skip Formspree entirely, you can drop in a **Flodesk inline form** instead. It handles the list-building natively but it uses Flodesk's own look, so the styling won't match as neatly. Tell me if you want that version and I'll build it.

---

## Part 3: Point the masterclass button at Humanitix

In `index.html`, find `REPLACE_WITH_HUMANITIX_LINK` and swap in your masterclass booking link. Re-upload the file.

*Note: the button currently shows the link as a placeholder attribute. Once you paste your real link in, tell me and I'll make the button open it, or you can change `href="#"` to your link in the same spot.*

---

## Updating the quiz later
Any time you want to change wording, edit `index.html` and re-upload it to the repo. The live page updates within a minute. Or just send me the change and I'll hand you a fresh file.
