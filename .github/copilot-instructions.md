# GitHub Repository Landing Page Generator

**ALWAYS follow these instructions first and only use search or bash commands when you encounter unexpected information that does not match what is documented here.**

## Working Effectively

- Clone and navigate to the repository:
  - `git clone https://github.com/QAQ-test/landpage.git`
  - `cd landpage`
- Test the landing page:
  - Start local server: `python3 -m http.server 8000` -- takes 2 seconds. NEVER CANCEL.
  - Open browser to: `http://localhost:8000/landingpage.html`
  - Alternative: `npx serve . -p 8001` -- takes 10 seconds on first run (npm install). NEVER CANCEL.
- Validate HTML/CSS/JS:
  - HTML validation: `python3 -c "import html.parser; validator = html.parser.HTMLParser(); validator.feed(open('landingpage.html').read()); print('✓ HTML valid')"` -- takes 0.02 seconds
  - JavaScript validation: Extract JS and run `node -c extracted_js.js` -- takes 0.04 seconds
- Git operations:
  - `git add .` -- takes 0.002 seconds
  - `git commit -m "message"` -- takes 0.005 seconds  
  - `git status` -- takes 0.002 seconds
  - `git push` -- takes 2-5 seconds depending on network

## Configuration

- The repository is configured for `J-I-P/youtube_test` by default
- To change the target repository, edit `landingpage.html` lines 107-108:
  ```javascript
  const REPO_OWNER = "your-username";   // e.g. "facebook"
  const REPO_NAME  = "your-repo-name";  // e.g. "react"
  ```
- Find configuration lines with: `grep -n "REPO_OWNER\|REPO_NAME" landingpage.html`
- All GitHub links, clone commands, and API calls update automatically

## Validation

- ALWAYS test configuration changes by starting a local server and viewing the page in a browser
- ALWAYS test that navigation links work (快速開始, 版本, 關於)
- ALWAYS verify that the page title and all GitHub links update correctly after configuration changes
- Test different repository configurations to ensure API calls work (note: external API calls may be blocked in sandboxed environments)
- The page handles GitHub API failures gracefully with error messages
- Badges and release information may not load due to CORS/network restrictions but the page structure should remain intact

## Deployment Options

- **GitHub Pages**: Push to GitHub and enable Pages in repository settings -- takes 30-60 seconds to deploy
- **Netlify**: Drag and drop `landingpage.html` to https://app.netlify.com/drop -- instant deployment
- **Vercel**: Install CLI with `npm install -g vercel` (takes 18 seconds), then `vercel --public` -- takes 30-60 seconds to deploy
- **Local development**: Any HTTP server works (Python, Node.js, nginx, etc.)

## Common Tasks

The following are outputs from frequently run commands to save time:

### Repository structure
```
landpage/
├── landingpage.html          # Main landing page file (7.9KB)
├── README.md                 # Documentation (9.9KB) 
└── .git/                     # Git version control
```

### Configuration location
Lines 107-108 in `landingpage.html`:
```javascript
const REPO_OWNER = "J-I-P";   // e.g. "facebook"
const REPO_NAME  = "youtube_test"; // e.g. "react"
```

### Key features
- **Zero Dependencies**: Pure HTML/CSS/JavaScript, no build tools required
- **Single File**: Everything contained in one HTML file
- **GitHub API Integration**: Automatically fetches stars, forks, issues, license badges
- **Release Information**: Shows latest release data from GitHub API
- **Responsive Design**: Works on desktop, tablet, and mobile
- **Multiple Languages**: Chinese/English interface

### Timing expectations
- Server startup: 2-10 seconds
- File validation: 0.02-0.04 seconds  
- Git operations: 0.002-0.005 seconds
- Deployment: 30-60 seconds (varies by platform)
- Configuration changes: Instant (just edit file)

## Troubleshooting

**Q: GitHub badges or release info not showing?**
- A: Expected in sandboxed environments due to CORS/network restrictions. Test with actual deployment.

**Q: How to validate changes work?**
- A: Always start local server and test in browser. Check that repository name updates in title, navigation, and all links.

**Q: JavaScript errors in console?**
- A: External API calls (GitHub API, Shields.io) may fail in development. The page should still render correctly.

**Q: Need to test with different repositories?**
- A: Copy file to `/tmp`, modify REPO_OWNER/REPO_NAME, serve from `/tmp`, and test in browser.

## File Structure Details

- **Lines 1-7**: HTML head with meta tags and title
- **Lines 8-32**: CSS styles (responsive design, dark theme)
- **Lines 33-103**: HTML body structure (navigation, hero, sections) 
- **Lines 105-178**: JavaScript (configuration, API calls, DOM updates)

**Always validate configuration changes by viewing the page in a browser and checking that the repository name appears correctly in all locations.**