# Deployment Guide - Restaurant Health Leaderboard

## Quick Start
1. Copy `index.html` to any web server or open directly in browser
2. No build process or dependencies required
3. Application is ready to use immediately

## Deployment Options

### Option 1: Local File System
```bash
# Simply open the file in any browser
open index.html
# or
firefox index.html
# or
chrome index.html
```

### Option 2: Static Web Hosting
**GitHub Pages:**
1. Create repository
2. Upload `index.html` to root
3. Enable GitHub Pages in repository settings
4. Access via `https://username.github.io/repository-name`

**Netlify:**
1. Drag and drop `index.html` to Netlify dashboard
2. Get instant deployment URL
3. Optional: Configure custom domain

**Vercel:**
```bash
npm i -g vercel
vercel --public
```

### Option 3: Web Server
**Apache/Nginx:**
- Copy `index.html` to web root directory (`/var/www/html/` or similar)
- Configure virtual host if needed
- Access via server URL

**Python Simple Server (for testing):**
```bash
# Python 3
python -m http.server 8000
# Python 2
python -m SimpleHTTPServer 8000
```

### Option 4: Trade Show/Demo Setup
**Recommended for presentations:**
1. Copy to USB drive or local laptop
2. Use Chrome/Firefox in full-screen mode (F11)
3. Set up on large display/projector
4. Test input methods (keyboard, touchscreen if available)

## Configuration Options

### Customization Variables
The following can be modified directly in `index.html`:

**Scoring Thresholds (lines 408-411):**
```javascript
if (restaurant.score >= 90) scoreClass = 'excellent';      // 90-100
else if (restaurant.score >= 80) scoreClass = 'good';      // 80-89  
else if (restaurant.score >= 70) scoreClass = 'fair';      // 70-79
// Below 70 = poor
```

**Animation Timing (line 413):**
```javascript
const isNew = Date.now() - restaurant.timestamp < 2000;    // 2 seconds pulse
```

**Visual Styling:**
- Colors: Modify CSS gradient values (lines 16, 84, 108, etc.)
- Fonts: Change font-family in body style (line 15)
- Sizing: Adjust responsive breakpoints (line 288)

### Environment-Specific Adjustments

**Trade Show/Demo Environment:**
- Increase font sizes for large displays
- Extend animation durations for better visibility
- Add keyboard shortcuts for quick demo flow

**Production Use (if extended):**
- Add data persistence (localStorage/backend)
- Implement form validation library
- Add accessibility features
- Consider framework migration

## Performance Optimization

### For Large Displays
```css
/* Add to existing styles for 4K+ displays */
@media (min-width: 2560px) {
    .header h1 { font-size: 4rem; }
    .leaderboard-entry { padding: 30px; }
    .score { font-size: 3rem; }
}
```

### For Touch Devices
```css
/* Enhance touch targets */
.add-btn, .delete-btn { 
    min-height: 44px; 
    min-width: 44px; 
}
```

## Troubleshooting

### Common Issues
1. **File won't open**: Ensure `.html` extension is preserved
2. **Styling issues**: Check browser compatibility (use modern browser)
3. **Input not working**: Verify JavaScript is enabled
4. **Mobile display problems**: Test responsive breakpoints

### Browser Support
- **Recommended**: Chrome 70+, Firefox 60+, Safari 12+, Edge 79+
- **Minimum**: Any browser with ES6 and Flexbox support

### Demo Day Checklist
- [ ] Test on target display/device
- [ ] Verify keyboard/mouse input works
- [ ] Practice demo flow (add/delete/clear operations)
- [ ] Have backup browser/device ready
- [ ] Test fullscreen mode (F11)
- [ ] Clear any existing data before starting

## Backup and Recovery
Since the application uses in-memory storage:
- Data is lost on page refresh (by design)
- No backup needed for demo use
- For persistent data, consider adding localStorage implementation

## Security Notes
- Safe for public demos (no data persistence)
- No external API calls or data transmission
- Client-side only execution
- No sensitive information stored or processed