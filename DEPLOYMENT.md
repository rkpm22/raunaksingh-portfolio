# GitHub Pages Deployment Guide

This guide will help you deploy your portfolio website to GitHub Pages.

## Prerequisites

- GitHub account
- Git installed on your computer
- Your portfolio files ready

## Step 1: Create a GitHub Repository

1. Go to [GitHub](https://github.com) and sign in
2. Click the "+" icon in the top right corner
3. Select "New repository"
4. Name your repository (recommended: `your-username.github.io`)
5. Make sure it's set to "Public"
6. Don't initialize with README (you already have files)
7. Click "Create repository"

## Step 2: Upload Your Files

### Option A: Using GitHub Web Interface
1. In your new repository, click "uploading an existing file"
2. Drag and drop all your portfolio files:
   - `index.html`
   - `styles.css`
   - `script.js`
   - `assets/` folder (if you have images)
   - Any other files
3. Add a commit message like "Initial portfolio upload"
4. Click "Commit changes"

### Option B: Using Git Command Line
```bash
# Navigate to your portfolio folder
cd /path/to/your/portfolio

# Initialize git repository
git init

# Add all files
git add .

# Make your first commit
git commit -m "Initial portfolio upload"

# Add your GitHub repository as origin
git remote add origin https://github.com/your-username/your-repo-name.git

# Push to GitHub
git branch -M main
git push -u origin main
```

## Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on "Settings" tab
3. Scroll down to "Pages" section in the left sidebar
4. Under "Source", select "Deploy from a branch"
5. Select "main" branch
6. Select "/ (root)" folder
7. Click "Save"

## Step 4: Access Your Website

1. GitHub will provide you with a URL like: `https://your-username.github.io/repository-name`
2. It may take a few minutes for the site to be available
3. You can find the URL in the "Pages" section of your repository settings

## Step 5: Custom Domain (Optional)

If you have a custom domain:

1. Create a file named `CNAME` in your repository root
2. Add your domain name (e.g., `www.yourname.com`)
3. Configure your domain's DNS settings to point to GitHub Pages
4. In repository settings > Pages, add your custom domain

## Updating Your Portfolio

To update your portfolio:

### Using GitHub Web Interface:
1. Navigate to the file you want to edit
2. Click the pencil icon to edit
3. Make your changes
4. Commit the changes

### Using Git Command Line:
```bash
# Make your changes to files
# Add changes
git add .

# Commit changes
git commit -m "Update portfolio content"

# Push to GitHub
git push origin main
```

## Customization Tips

### Update Personal Information
1. Edit `index.html` to update:
   - Your name and title
   - About section content
   - Experience details
   - Skills
   - Project information
   - Contact information

### Add Your Images
1. Add your photos to the `assets/` folder
2. Update the image paths in `index.html`:
   - Replace placeholder URLs with `assets/your-image.jpg`
   - Update alt text for accessibility

### Customize Colors and Styling
1. Edit `styles.css` to change:
   - Color scheme (look for CSS custom properties at the top)
   - Fonts
   - Spacing
   - Animations

### Update Content
1. Add your actual projects with:
   - Real project descriptions
   - Actual GitHub/demo links
   - Technologies used
   - Screenshots

## SEO Optimization

Add these meta tags to your `<head>` section in `index.html`:

```html
<meta name="description" content="Your Name - Full Stack Developer Portfolio">
<meta name="keywords" content="web developer, full stack, portfolio, your-name">
<meta name="author" content="Your Name">
<meta property="og:title" content="Your Name - Portfolio">
<meta property="og:description" content="Full Stack Developer Portfolio">
<meta property="og:image" content="https://your-username.github.io/assets/profile-hero.jpg">
<meta property="og:url" content="https://your-username.github.io">
```

## Performance Tips

1. **Optimize Images**:
   - Compress images before uploading
   - Use WebP format for better compression
   - Keep file sizes under 500KB

2. **Minimize Files**:
   - Remove unnecessary code
   - Use compressed versions of libraries

3. **Add Analytics**:
   - Add Google Analytics tracking code
   - Monitor your site's performance

## Troubleshooting

### Site Not Loading
- Check if GitHub Pages is enabled in settings
- Ensure `index.html` is in the root directory
- Wait 10-15 minutes for changes to propagate

### Images Not Showing
- Verify image paths are correct
- Check if images are uploaded to the repository
- Ensure image file names match exactly (case-sensitive)

### Custom Domain Issues
- Verify DNS settings
- Check CNAME file content
- Wait for DNS propagation (up to 24 hours)

## Security Considerations

1. **Never commit sensitive information**:
   - API keys
   - Passwords
   - Personal phone numbers or addresses

2. **Use environment variables** for sensitive data
3. **Be careful with contact forms** - use services like Formspree or Netlify Forms

## Advanced Features

### Add a Blog
1. Create a `blog/` folder
2. Add HTML files for blog posts
3. Update navigation to include blog link

### Add Google Analytics
```html
<!-- Add before closing </head> tag -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_TRACKING_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_TRACKING_ID');
</script>
```

### Add Contact Form
Use services like:
- Formspree
- Netlify Forms
- EmailJS

## Support

If you encounter issues:
1. Check GitHub Pages documentation
2. Verify your repository settings
3. Check the repository's "Actions" tab for build errors
4. Contact GitHub support if needed

## Final Checklist

Before going live:
- [ ] Update all personal information
- [ ] Add your actual photos
- [ ] Update project descriptions and links
- [ ] Test all links and functionality
- [ ] Add contact information
- [ ] Optimize images
- [ ] Test on different devices
- [ ] Check for typos and grammar
- [ ] Add meta tags for SEO
- [ ] Test form functionality (if applicable)

Your professional portfolio is now ready to showcase your skills to the world! 🚀 