# Workspace3 - Web Version

A web application wrapper for the Meshy AI Workspace, designed to be deployed on Vercel.

## Overview

This is a web version of the Workspace3 mobile app that provides access to Meshy AI's workspace functionality through a responsive web interface.

## Features

- **Responsive Design**: Works on desktop, tablet, and mobile devices
- **Navigation Menu**: Access to all Meshy AI features and pages
- **Dark Mode Support**: Automatically adapts to system preferences
- **Security Headers**: Includes appropriate security headers for web deployment
- **Loading States**: Provides feedback while content loads

## Deployment

### Deploy to Vercel (Recommended)

1. **Connect to GitHub**: Link your repository to Vercel
2. **Import Project**: Import this repository in your Vercel dashboard
3. **Deploy**: Vercel will automatically detect the configuration and deploy

#### Manual Deployment

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy to Vercel
vercel

# For production deployment
vercel --prod
```

### Deploy to Netlify

1. Connect your repository to Netlify
2. Set build settings:
   - Build command: `echo "Static site - no build needed"`
   - Publish directory: `/` (root)

### Deploy to Other Static Hosts

This is a static HTML application and can be deployed to any static hosting service:
- GitHub Pages
- AWS S3 + CloudFront
- Google Cloud Storage
- Any CDN or static hosting service

## Local Development

```bash
# Serve locally using Node.js
npm run dev

# Or using Python
python -m http.server 8000

# Or using any static file server
```

## Configuration

The application includes:

- **`vercel.json`**: Vercel-specific configuration for routing and headers
- **`package.json`**: Node.js package configuration for development
- **`index.html`**: Main application file with embedded CSS and JavaScript

## Architecture

- **Static HTML/CSS/JS**: No build process required
- **Iframe Integration**: Embeds the Meshy AI workspace
- **Responsive Layout**: Mobile-first design approach
- **Security**: Appropriate headers and iframe sandboxing

## Browser Support

- Chrome/Chromium (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Security

The application includes several security measures:
- Content Security Policy headers
- Iframe sandboxing
- Referrer policy configuration
- XSS protection headers

## Troubleshooting

### Iframe Loading Issues

If the Meshy AI workspace doesn't load in the iframe:

1. **CORS Restrictions**: Some sites prevent iframe embedding
2. **Ad Blockers**: May block iframe content
3. **Network Issues**: Check your internet connection

**Solution**: The app provides a fallback link to open Meshy AI directly.

### Deployment Issues

1. **Build Errors**: This is a static site with no build process
2. **Routing Issues**: Ensure `vercel.json` is properly configured
3. **HTTPS Required**: Most modern features require HTTPS

## License

MIT License - see LICENSE file for details.

## Support

For issues with:
- **Web App**: Create an issue in this repository
- **Meshy AI Platform**: Visit [help.meshy.ai](https://help.meshy.ai/en/)