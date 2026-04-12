# Deploying the Θ(n²) Visualization to GitHub Pages

## Repository setup

1. In the `clarkCollege-CSE-SoftwareEngineering` GitHub org, create a new repository — e.g., **`cse320-visualizations`**.
2. Upload `theta_notation.html` to the root of the repository (or a `visualizations/` subfolder if you plan to add more).
3. Commit and push.

## Enable GitHub Pages

1. Go to **Settings → Pages** in the repository.
2. Under *Source*, select **Deploy from a branch**.
3. Choose **`main`** branch and **`/ (root)`** folder (or `/visualizations` if you used a subfolder). Click **Save**.
4. GitHub will publish the site within ~60 seconds. The URL will be:

```
https://clarkcollege-cse-softwareengineering.github.io/cse320-visualizations/theta_notation.html
```

The visualization loads React/Recharts entirely from CDN — no build step is required.

## Embedding in a Canvas LMS page

1. In your Canvas course, go to **Pages → + Page**.
2. In the Rich Content Editor toolbar, click the **`< >`** (HTML Editor) button.
3. Paste the following `<iframe>` tag, replacing the URL with your actual GitHub Pages URL:

```html
<iframe
  src="https://clarkcollege-cse-softwareengineering.github.io/cse320-visualizations/theta_notation.html"
  width="100%"
  height="840"
  style="border:none; border-radius:10px;"
  title="Theta Notation Tight Bound Visualization">
</iframe>
```

4. Switch back to the visual editor and Save & Publish.

## Sharing via Canvas Course Commons

Because the iframe URL points to a stable GitHub org URL (not a personal account or course-specific file), this page is safe to share to Course Commons:

1. From the Canvas page, click **Share to Commons** (or use the course export flow).
2. Any future instructor who imports the page from Commons will get the iframe pointing to the same GitHub Pages URL — no re-hosting required.

**To ensure long-term availability**, keep the `cse320-visualizations` repository under the department GitHub org rather than a personal account, so it persists across instructor transitions.

## Adding more visualizations

To add additional visualizations later, upload more `.html` files to the same repository and they will automatically be served at `…github.io/cse320-visualizations/<filename>.html`. Update this README with the new iframe snippets as you go.
