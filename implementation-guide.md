# Wanaka FC Performance Optimization - Implementation Guide

## Quick Start (5 minutes)

### Step 1: Replace Main File
1. **Backup** your current `index.html`
2. **Replace** with `optimized-index.html`
3. **Test** the new version

### Step 2: Add New Files
1. **Copy** all new files to your project root:
   - `performance-optimization.css`
   - `performance-optimization.js`
   - `critical-css.html`
   - `preload-manifest.json`

### Step 3: Update Image Tags
Add these attributes to all `<img>` tags:
```html
<img src="image.jpg" 
     alt="Description" 
     loading="lazy" 
     width="400" 
     height="300">
```

## Detailed Implementation

### Phase 1: Image Optimization (2 minutes)
1. Add `loading="lazy"` to all non-critical images
2. Add `width` and `height` attributes to prevent layout shifts
3. Add `decoding="async"` for better performance

### Phase 2: CSS Optimization (3 minutes)
1. **Inline critical CSS** in `<head>` (copy from `critical-css.html`)
2. **Defer non-critical CSS** using media trick
3. **Preload key resources** with `<link rel="preload">`

### Phase 3: JavaScript Optimization (2 minutes)
1. **Add defer attribute** to all script tags
2. **Implement lazy loading** for images and components
3. **Add loading screen** for better user experience

## Testing Performance

### Lighthouse Testing
1. Open Chrome DevTools (F12)
2. Go to Lighthouse tab
3. Run audit on mobile and desktop
4. Target scores:
   - Performance: 90+
   - Accessibility: 95+
   - Best Practices: 95+
   - SEO: 95+

### Manual Testing
1. **Network throttling**: Test on 3G connection
2. **Device testing**: Check on mobile devices
3. **Browser testing**: Verify in Chrome, Firefox, Safari, Edge

## Common Issues & Solutions

### Images Not Loading
- **Solution**: Check file paths and ensure images exist
- **Debug**: Use browser dev tools Network tab

### Layout Shifts
- **Solution**: Ensure all images have width/height attributes
- **Debug**: Use Lighthouse Layout Shift audit

### Slow Loading
- **Solution**: Verify preload links are correct
- **Debug**: Check resource loading order in Network tab

## Rollback Plan
If issues occur:
1. **Restore** original `index.html` from backup
2. **Remove** new CSS and JS files
3. **Revert** image tag changes
4. **Test** functionality is restored

## Support
For implementation help:
1. Check `performance-report.md` for detailed explanations
2. Review browser console for errors
3. Test in incognito mode to avoid caching issues
