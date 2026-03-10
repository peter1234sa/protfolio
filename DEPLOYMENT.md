# Vercel Deployment Guide

This guide will help you deploy your portfolio website to Vercel.

## Prerequisites
- A Vercel account (sign up at https://vercel.com)
- Git installed on your system
- Your project should be in a Git repository

## Method 1: Deploy via Vercel Dashboard (Easiest)

### Step 1: Push to GitHub (if not already done)
```bash
cd /Users/tushirsahu/Desktop/loakeshbachhu.github.io
git add .
git commit -m "Prepare for Vercel deployment"
git push origin main
```

### Step 2: Deploy via Vercel Dashboard
1. Go to https://vercel.com and sign in
2. Click "Add New Project"
3. Import your GitHub repository (loakeshbachhu/loakeshbachhu.github.io)
4. Configure the project:
   - Framework Preset: **Other** (or None)
   - Root Directory: **./** (leave as default)
   - Build Command: **leave empty** (static site, no build needed)
   - Output Directory: **./** (leave as default)
5. Click "Deploy"
6. Your site will be live in 1-2 minutes!

## Method 2: Deploy via Vercel CLI

### Step 1: Install Vercel CLI
```bash
npm install -g vercel
```

### Step 2: Login to Vercel
```bash
vercel login
```

### Step 3: Deploy
```bash
cd /Users/tushirsahu/Desktop/loakeshbachhu.github.io
vercel
```

Follow the prompts:
- Set up and deploy? **Y**
- Which scope? Select your account
- Link to existing project? **N**
- What's your project's name? **tushir-portfolio** (or any name)
- In which directory is your code located? **./**
- Want to modify settings? **N**

### Step 4: Deploy to Production
```bash
vercel --prod
```

## Method 3: Deploy via Drag & Drop

1. Go to https://vercel.com/new
2. Click on "Deploy without Git"
3. Drag and drop your project folder
4. Click "Deploy"

## After Deployment

### Your Site URLs
- Production: `https://your-project-name.vercel.app`
- You can add a custom domain in Vercel dashboard

### Updating Your Site
- **With Git**: Just push to your repository, Vercel auto-deploys
- **With CLI**: Run `vercel --prod` in your project directory

## Project Structure Verified
```
loakeshbachhu.github.io/
├── index.html          ✓ Main HTML file
├── favicon.ico         ✓ Favicon
├── css/
│   └── style.css       ✓ Styles
├── js/
│   ├── main.js         ✓ Main JavaScript
│   ├── Typewriter.js   ✓ Typewriter library
│   └── winbox.bundle.js ✓ WinBox library
├── vercel.json         ✓ Vercel configuration (newly added)
└── .vercelignore       ✓ Files to ignore (newly added)
```

## Notes

### Missing File Alert
⚠️ Your `index.html` references `Loakesh Bachhu CV.pdf` but this file is not in the project.
Either:
1. Add the PDF file to your project root, OR
2. Remove/update the resume link in `index.html`

### Environment Variables
No environment variables needed for this static site.

### Custom Domain (Optional)
1. Go to your project in Vercel dashboard
2. Click "Settings" → "Domains"
3. Add your custom domain
4. Update your DNS records as instructed

## Troubleshooting

### Issue: 404 Errors
- Make sure `index.html` is in the root directory
- Check that all file paths are relative (no leading /)

### Issue: CSS/JS Not Loading
- Verify file paths in `index.html`
- Check browser console for errors

### Issue: Deployment Fails
- Check Vercel deployment logs
- Ensure all referenced files exist

## Quick Deploy Command (After CLI Setup)
```bash
cd /Users/tushirsahu/Desktop/loakeshbachhu.github.io
vercel --prod
```

Your portfolio will be live at: `https://your-project-name.vercel.app`

## Support
- Vercel Docs: https://vercel.com/docs
- Vercel Support: https://vercel.com/support
