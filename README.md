# Berlin Piano Society

The website for the Berlin Piano Society — plain HTML/CSS, no build step, hosted on GitHub Pages.

## Files

| File          | What it is                                            |
| ------------- | ----------------------------------------------------- |
| `index.html`  | Home page                                             |
| `about.html`  | About / membership                                    |
| `events.html` | Events list (copy a `.event` block to add an entry)   |
| `contact.html`| Contact details                                       |
| `styles.css`  | All styling — edit colours and fonts at the top       |
| `CNAME`       | Tells GitHub Pages to serve `berlinpianosociety.com`  |

Anything marked `<!-- EDIT: ... -->` in the HTML is placeholder copy to replace.

## Editing

Open any `.html` file in a text editor and change the text. No tooling needed.
To preview locally, just open the file in a browser, or run a tiny server:

```bash
python3 -m http.server   # then visit http://localhost:8000
```

## Going live (one-time setup)

### 1. Turn on GitHub Pages
Repo → **Settings → Pages** → *Build and deployment* → Source: **Deploy from a branch**,
Branch: **main**, folder: **/ (root)** → Save.
Your site appears at `https://simonredfern.github.io/berlin-piano-society/`.

### 2. Point the domain (Namecheap → Advanced DNS)
Delete Namecheap's default parking records first, then add:

| Type  | Host | Value                  |
| ----- | ---- | ---------------------- |
| A     | @    | 185.199.108.153        |
| A     | @    | 185.199.109.153        |
| A     | @    | 185.199.110.153        |
| A     | @    | 185.199.111.153        |
| CNAME | www  | simonredfern.github.io |

### 3. Set the custom domain
Repo → **Settings → Pages → Custom domain** → enter `berlinpianosociety.com` → Save.
Wait for the DNS check to pass (minutes to a few hours), then tick **Enforce HTTPS**.

The `CNAME` file in this repo already holds the domain, so Pages keeps the setting
across pushes.
