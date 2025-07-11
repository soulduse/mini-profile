# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static personal profile website for "프로그래밍좀비" (Programming Zombie), showcasing developer achievements and featuring interactive elements. The project is deployed on AWS (S3 + CloudFront).

## Technology Stack

- **Frontend**: Pure HTML, CSS (Tailwind CSS via CDN), Vanilla JavaScript
- **No build system**: Direct static file editing
- **External Libraries**:
  - Tailwind CSS 2.2.19 (CDN)
  - Cropper.js (for santa-hat feature)
  - html2canvas (for image export)
  - Google Analytics

## Project Structure

```
/mini-profile/
├── profile.html       # Main profile page with dark theme
├── santa-hat/         # Christmas feature
│   ├── index.html     # Interactive Santa hat photo editor
│   └── santa_hat.png  # Hat overlay image
└── README.md          # Korean documentation
```

## Development Guidelines

### No Build Process
This is a static website - edit HTML/CSS/JS files directly. There's no package.json or build commands.

### Testing
Open HTML files directly in a browser. For the santa-hat feature, test:
- Image upload and cropping
- Touch controls on mobile
- Export functionality

### Key Implementation Details

**Profile Page (profile.html)**:
- Uses CSS custom properties for theming
- Implements analytics tracking with `gtag` events
- Responsive design with Tailwind utilities
- Glassmorphism effects with backdrop filters

**Santa Hat Feature (santa-hat/index.html)**:
- Mobile-first design with touch event handling
- Image processing workflow: upload → crop → position hat → export
- Uses Canvas API for image manipulation
- Maintains 1:1 aspect ratio for profile pictures

### Code Conventions

- Korean language for UI text and comments
- Event tracking on all interactive elements
- Inline styles mixed with Tailwind classes
- Use `addEventListener` for event handling
- Mobile-responsive design is required

### Deployment

The site is deployed on AWS:
- S3 for static hosting
- CloudFront for CDN
- No CI/CD pipeline - manual upload to S3

### Important Notes

- All external assets (profile images, etc.) are referenced via URLs
- The project was developed with AI assistance (Claude) in approximately 2 hours
- Focus on simplicity and performance - avoid adding unnecessary dependencies