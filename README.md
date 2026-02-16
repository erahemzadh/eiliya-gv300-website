# Personal Website - GV300 Showcase

This repository contains the source code for my personal website, built with [Distill](https://rstudio.github.io/distill/) and [Postcards](https://github.com/seankross/postcards) for R Markdown.

## 🌐 Live Site

View the live site at: `https://your-github-username.github.io/your-repo-name`

## 📁 Repository Structure

```
your-repo-name/
├── _site.yml              # Site configuration
├── index.Rmd              # Homepage (Postcards landing page)
├── about.Rmd              # About page
├── gv300-showcase.Rmd     # GV300 work showcase
├── theme.css              # Custom CSS styling
├── README.md              # This file
├── .gitignore            # Git ignore file
└── docs/                  # Rendered site (auto-generated)
```

## 🚀 Quick Start

### Prerequisites

- R (>= 4.0)
- RStudio
- Git
- GitHub account

### Required R Packages

```r
install.packages(c("distill", "postcards", "tidyverse", "ggplot2", "knitr"))
```

## 📝 Setup Instructions

### 1. Create the RStudio Project

1. Open RStudio
2. File → New Project → New Directory → Distill Website
3. Name your project and choose location
4. Check "Create a git repository"

### 2. Add the Template Files

Copy these files into your project directory:

- `_site.yml`
- `index.Rmd`
- `about.Rmd`
- `gv300-showcase.Rmd`
- `theme.css`

**IMPORTANT: Also add your data file:**
- Copy `kidiq-2.csv` from Assignment 1 to your project directory
- The UK election data loads automatically from the Parliament website
- The A/B test uses simulated data (matching your Assignment 3 approach)

### 3. Customize Your Content

**In `_site.yml`:**
- Replace `your-github-username` with your actual GitHub username
- Replace `your-repo-name` with your repository name
- Update the title to your name

**In `index.Rmd`:**
- Add your name and photo
- Update links (LinkedIn, GitHub, Email)
- Write your bio
- Add your university and programme

**In `about.Rmd`:**
- Fill in your background
- List your skills and interests
- Update contact information

**In `gv300-showcase.Rmd`:**
- Replace simulated data with your actual assignment data
- Add your real code from Assignments 1-3
- Update visualizations with your work
- Personalize the narrative

### 4. Add a Profile Photo (Optional)

1. Add an image file named `profile.jpg` to your project root
2. Or update `index.Rmd` to reference your image filename

### 5. Build the Site Locally

In RStudio Console:

```r
# Render the site
rmarkdown::render_site()
```

Or use the "Build" tab in RStudio:
- Click "Build Website"

This creates a `docs/` folder with your rendered site.

### 6. Set Up GitHub Repository

```bash
# Initialize git (if not already done)
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit - personal website"

# Create repository on GitHub, then:
git remote add origin https://github.com/your-username/your-repo-name.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### 7. Enable GitHub Pages

1. Go to your repository on GitHub
2. Settings → Pages
3. Source: Deploy from a branch
4. Branch: `main`
5. Folder: `/docs`
6. Save

Your site will be live at `https://your-username.github.io/your-repo-name` in a few minutes!

### 8. Update `_site.yml` Base URL

Once your site is live, update the `base_url` in `_site.yml`:

```yaml
base_url: https://your-username.github.io/your-repo-name
```

Then rebuild and push:

```r
rmarkdown::render_site()
```

```bash
git add .
git commit -m "Update base URL"
git push
```

## 🔄 Updating Your Site

Whenever you make changes:

1. **Edit** your `.Rmd` files in RStudio
2. **Build** the site: `rmarkdown::render_site()` or use Build tab
3. **Commit** changes:
   ```bash
   git add .
   git commit -m "Update content"
   git push
   ```
4. **Wait** 1-2 minutes for GitHub Pages to rebuild

## 🎨 Customization Tips

### Change Postcards Theme

In `index.Rmd`, you can use different Postcards themes:

```yaml
output:
  postcards::trestles  # Current theme
  # postcards::jolla
  # postcards::onofre
  # postcards::solana
```

### Modify Colors

Edit `theme.css` to change:
- Primary color: Change `#0066cc` throughout
- Fonts: Update `@import` and `font-family` declarations
- Spacing: Adjust margins and padding

### Add New Pages

1. Create new `.Rmd` file (e.g., `blog.Rmd`)
2. Add to `_site.yml` navbar:
   ```yaml
   - text: "Blog"
     href: blog.html
   ```
3. Rebuild site

## 📚 Resources

- [Distill Documentation](https://rstudio.github.io/distill/)
- [Postcards Package](https://github.com/seankross/postcards)
- [Setup Guide by Alison Hill](https://www.apreshill.com/blog/2020-12-postcards-distill/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [R Markdown Guide](https://rmarkdown.rstudio.com/)

## 🐛 Troubleshooting

### Site won't build
- Check all `.Rmd` files knit individually
- Look for errors in R Console
- Ensure all packages are installed

### GitHub Pages shows 404
- Verify GitHub Pages is enabled
- Check that `/docs` folder is in repository
- Ensure branch is set to `main` and folder to `/docs`

### Images not displaying
- Check file paths are correct
- Ensure images are in the repository
- Use relative paths (not absolute)

### Code chunks not running
- Check chunk options
- Verify required packages are loaded
- Look for syntax errors in R code

## 📧 Contact

Questions about this website? Reach out:

- **Email**: your.email@example.com
- **GitHub**: [@your-username](https://github.com/your-username)

## 📄 License

This website template is available for personal and educational use. Feel free to fork and adapt!

---

*Built with ❤️ using R, Distill, and Postcards*
