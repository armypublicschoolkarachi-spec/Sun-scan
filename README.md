# Sun Scan

A mobile-friendly, dark blue manhwa archive demo inspired by common scanlation-site layouts. It is a static website, so it can be hosted for free with GitHub Pages.

## Included
- Responsive homepage and featured series
- Search by title, genre filters, sorting, and latest updates
- Series detail modal with synopsis and chapter list
- Vertical scrolling chapter-reader layout (demo placeholder panels)
- My List saved in the browser with `localStorage`
- Reading progress stored locally in the browser
- No build tools or package installation required

## Put it on GitHub from your Android phone

1. Download and unzip `sun-scan.zip` on your phone.
2. Open **github.com** in your browser and sign in.
3. Tap **+** → **New repository**.
4. Name it `sun-scan`. Choose **Public** if you want GitHub Pages on the free plan, then create the repository.
5. Open the new repository and choose **Add file** → **Upload files**.
6. Upload `index.html`, `styles.css`, `app.js`, and this `README.md` from the unzipped folder. (You can upload the `assets` folder too if you later add images.)
7. Commit the upload.
8. Open repository **Settings** → **Pages**.
9. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/(root)`, then save.
10. Wait for GitHub Pages to publish. The URL will look like `https://YOUR-USERNAME.github.io/sun-scan/`.

If you edit the site, upload the changed file(s) and commit again. GitHub Pages updates automatically after the deployment finishes.

## How to add a series

Open `app.js` and find the `const SERIES = [` list near the top. Copy one series object and change its `id`, `title`, `genres`, `chapter`, `updated`, `cover`, `orb`, `synopsis`, and `chapters`.

Example:
```js
{
  id: "my-new-series",
  title: "My New Series",
  genres: ["Action", "Fantasy"],
  status: "Ongoing",
  chapter: 1,
  updated: "2026-10-19",
  label: "NEW",
  featured: false,
  cover: "linear-gradient(145deg,#164c75,#07101d 78%)",
  orb: "#69baff",
  synopsis: "Write your series summary here.",
  chapters: [1]
}
```

Use a unique `id`. The `chapters` array lists the demo chapter numbers. It is shown newest first.

## How to add real chapter images

This starter version demonstrates the reader UI using placeholder panels. To show real chapter images, add image files to your repository (for example, `assets/my-series/chapter-1/01.jpg`) and change the reader rendering in `app.js` to output an `<img>` for each page in order. Use only images and translations you own or have permission to distribute.

## Important limitations

This is a **static front-end demo**, not a production publishing system:
- Adding a series or chapter currently requires editing `app.js`.
- The reader's panels are placeholders; real chapter files are not included.
- Saved titles and reading progress live in the current browser only; they do not sync between devices or accounts.
- There is no user login, admin dashboard, comments, or database yet.
- Google Fonts are loaded from an external service; if unavailable, fallback fonts are used.

Do not upload copyrighted chapters, translations, or cover artwork unless you have the rights or permission to distribute them.
