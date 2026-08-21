# Boutiqaat: The Influence Game

A browser-based teaching simulation on influencer-led commerce: creator networks and value capture, own labels versus brand partners, screens versus stores, and how far a culturally embedded model travels.

- **`boutiqaat-student.html`** — the page students play on.
- **`boutiqaat-instructor.html`** — the instructor console, behind a username and password.
- **`index.html`** — a landing page pointing at the student page.
- **`backend-google-apps-script.gs`** — the Google Sheet backend that collects results.

No build step, no dependencies, and nothing to install. Students need only a browser.

---

## Putting this online with GitHub Pages

### 1. Create the repository

On github.com, click **New repository**.

- Name it something students will not mind seeing in a URL, e.g. `strategy-sims`
- Set it to **Public**
- Tick **Add a README file**
- Click **Create repository**

> Public is what makes Pages free. Nothing sensitive lives in these files — no case text, no student data, no passcode. If your institution requires a private repository, GitHub Pages on private repos needs a paid plan.

### 2. Upload the files

On the repository page, click **Add file → Upload files**, then drag in:

```
index.html
boutiqaat-student.html
boutiqaat-instructor.html
backend-google-apps-script.gs
```

Add the guides too if you like — they do no harm and keep everything together.

Scroll down and click **Commit changes**.

### 3. Turn on Pages

Go to **Settings → Pages** in the repository.

- **Source:** Deploy from a branch
- **Branch:** `main`, folder `/ (root)`
- Click **Save**

Wait one or two minutes. The page will show your address:

```
https://YOUR-USERNAME.github.io/strategy-sims/
```

### 4. Check it works

Open that address. You should see the landing page. Click into a simulation and confirm it loads.

### 5. Connect a results backend

Without one, students play normally but send you a result code at the end. To have results arrive automatically, follow `HOSTING.md` — the Google Sheet route takes about ten minutes and is free.

Open **`boutiqaat-instructor.html`**, paste the endpoint URL, press **Test the connection**, then create your username and password. Then create your class.

### 6. Share one link with students

Copy the **student link** from the instructor console. It looks like:

```
https://YOUR-USERNAME.github.io/strategy-sims/boutiqaat-student.html#class=BTQ-2026A&backend=http&api=https://script.google.com/macros/s/AKfy.../exec
```

You can also point it at the landing page — the settings carry through:

```
https://YOUR-USERNAME.github.io/strategy-sims/#class=BTQ-2026A&backend=http&api=https://script.google.com/macros/s/AKfy.../exec
```

---

## Updating a file later

Click the file in GitHub, then the pencil icon to edit, or use **Add file → Upload files** and upload a replacement with the same name. Pages redeploys within a minute. Students may need a hard refresh (Ctrl-F5, or Cmd-Shift-R on a Mac) to clear the cached version.

## Using git from the command line instead

```bash
git clone https://github.com/YOUR-USERNAME/strategy-sims.git
cd strategy-sims
cp /path/to/*.html .
git add .
git commit -m "Add simulations"
git push
```

Then turn on Pages as in step 3.

---

## Reuse across cohorts

Give each cohort its own class code — `BTQ-2026A`, `BTQ-2026B`, and so on. Creating a new class never overwrites an old one, and the instructor console lists every class you have created so you can reopen past results. Full detail in `HOSTING.md`.

## Documentation

| File | What it covers |
|---|---|
| `HOSTING.md` | Storage backends, class reuse, troubleshooting |
| `Boutiqaat-Instructor-Guide.md` | Running the simulation, model detail, debrief plan |
| `Boutiqaat-Student-Guide.md` | Student handout |
| `backend-google-apps-script.gs` | Paste-in Google Sheet backend |
