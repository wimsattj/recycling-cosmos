# The Recycling Cosmos — Web Hub

This is the central landing page for The Recycling Cosmos research, fundraising campaigns, and article series.

## What is this?

A clean, simple website that serves as the hub for:
- **Article series** (links to Substack)
- **The research paper** (link to Zenodo)
- **Fundraising campaigns** (GoFundMe links)
- **Social media** (Facebook page)

## File Structure

```
web/
├── index.html          # Main landing page
├── css/
│   └── style.css       # All styling (responsive, clean design)
├── campaigns/          # Future: subfolder for each campaign
│   └── campaign-1/     # Example structure (add as needed)
│       ├── index.html
│       └── index.css
└── README.md           # This file
```

## How to Update

### Adding a new article link
Edit `index.html` in the "Read the Article Series" section. Find the article placeholder and update:
- The title (h3)
- The description (p)
- The Substack URL (change `https://substack.com/` to the actual article URL)
- Change "Coming soon →" to "Read on Substack →" when published

Example:
```html
<div class="article-item">
    <h3>Article 3: Why does the universe have a temperature?</h3>
    <p>The cosmic microwave background in plain English — gravitational lensing caustics, not primordial radiation.</p>
    <a href="https://substack.com/@therecyclingcosmos/article-3-slug" target="_blank">Read on Substack →</a>
</div>
```

### Adding Substack Newsletter signup
When your Substack is set up, add an inline signup form. Substack provides embed code — paste it in the "Connect With Us" section.

### Updating campaign information
Edit the "Support This Work" section to:
- Change GoFundMe URL (find the actual URL)
- Update goal amounts and timelines
- Add new campaigns as they launch

### Updating the Zenodo link
If you upload a new version to Zenodo, update:
- The DOI (currently 10.5281/zenodo.19477470)
- The date (currently April 8 2026)
- The URL link

## Deploying to GitHub Pages

This repo already uses GitHub. To enable GitHub Pages:

1. **Push the `web/` folder to GitHub** (should already be done after you commit)

2. **Enable Pages in your repo settings:**
   - Go to: `https://github.com/your-username/Universe-Expansion/settings/pages`
   - Under "Source", select:
     - Branch: `main`
     - Folder: `/web`
   - Click "Save"

3. **Your site will be live at:**
   - `https://your-username.github.io/Universe-Expansion/`
   - OR custom domain if you add one

4. **That's it.** Push changes to main, and they auto-deploy within minutes.

## Customization

The site uses CSS variables for easy rebranding:
```css
:root {
    --primary: #1e40af;      /* Deep blue */
    --secondary: #7c3aed;    /* Purple */
    --accent: #0891b2;       /* Cyan */
}
```

Change these in `css/style.css` to update colors site-wide.

## Testing Locally

Before pushing, test locally:
```bash
cd /home/yessenia/Documents/Universe.Expansion/web
# Mac/Linux: python3 -m http.server 8000
# Then visit: http://localhost:8000
```

## Structure for Multiple Campaigns

As you add more fundraising campaigns, create subfolders:
```
web/
├── index.html          # Hub (links to campaigns)
├── campaigns/
│   ├── publication-2026/
│   │   └── index.html  # Campaign 1 details
│   └── validation-2027/
│       └── index.html  # Campaign 2 details
```

Each campaign can have its own page with specific GoFundMe link, timeline, and goals.

## Notes

- **No database needed.** This is pure HTML/CSS — completely static.
- **No cost.** GitHub Pages hosting is free for public repos.
- **Fast deployment.** Changes go live in ~2 minutes after git push.
- **Mobile-friendly.** Design is responsive (tested down to 320px width).

---

**Questions?** Check GitHub Pages docs: https://docs.github.com/en/pages
