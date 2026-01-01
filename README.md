# HTML Overlay Themes

A collection of beautiful, interactive HTML overlays for special occasions.

## 📦 Available Overlays

1. **🎄 Christmas Overlay** (`christmas.html`)
   - Falling snow animation
   - Twinkling Christmas lights with string
   - Santa peeking from bottom
   - Responsive design

2. **🎆 New Year Overlay** (`newyear.html`)
   - Golden corner text with shimmer effect
   - Click-to-confetti animation (Hold Shift + Click)
   - Elegant vignette effect
   - Responsive design

3. **🎃 Halloween Overlay** (`halloween.html`)
   - Spooky Halloween theme
   - Interactive elements

## 🧪 Testing Your Overlays

Use the `test-page.html` to test all overlays with real form components, buttons, and links.

### How to Use with raw.githack CDN:

1. **Push your files to GitHub**
   ```bash
   git add .
   git commit -m "Add overlay files"
   git push origin main
   ```

2. **Get your raw.githack URL**
   - Go to [raw.githack.com](https://raw.githack.com/)
   - Enter your GitHub repository URL
   - Copy the **production** CDN URL (e.g., `https://raw.githack.com/RA-L-PH/html-themes/main/`)

3. **Open test-page.html**
   - Open `test-page.html` in your browser
   - Paste your raw.githack base URL in the CDN input field
   - Click any overlay button to load it dynamically

4. **Test interactions**
   - Fill out form fields
   - Click buttons
   - Interact with links
   - Verify the overlay doesn't interfere with page functionality

### Example CDN URL Format:
```
https://raw.githack.com/YOUR-USERNAME/YOUR-REPO/main/
```

## 🎨 Using Overlays in Your Projects

### Method 1: Direct Include (Local)
```html
<!-- Include the overlay HTML file content directly -->
<div id="overlay-container">
    <!-- Paste content from christmas.html, newyear.html, etc. -->
</div>
```

### Method 2: Dynamic Loading (CDN)
```html
<div id="overlay-container"></div>

<script>
function loadOverlay(type) {
    const cdnBaseUrl = 'https://raw.githack.com/YOUR-USERNAME/YOUR-REPO/main/';
    const overlayUrl = `${cdnBaseUrl}${type}.html`;
    
    fetch(overlayUrl)
        .then(response => response.text())
        .then(html => {
            document.getElementById('overlay-container').innerHTML = html;
        })
        .catch(error => console.error('Error loading overlay:', error));
}

// Load Christmas overlay
loadOverlay('christmas');
</script>
```

### Method 3: iframe (Simple but Limited)
```html
<iframe src="https://raw.githack.com/YOUR-USERNAME/YOUR-REPO/main/christmas.html" 
        style="position:fixed;top:0;left:0;width:100%;height:100%;border:none;pointer-events:none;z-index:9999;">
</iframe>
```

## 🎯 Features

- **Zero Dependencies**: Pure HTML, CSS, and JavaScript
- **Responsive Design**: Works on all screen sizes
- **Non-Intrusive**: `pointer-events: none` ensures overlays don't block interactions
- **Lightweight**: Optimized for performance
- **Easy Integration**: Simple copy-paste or CDN loading

## 📝 Customization

Each overlay file is self-contained with:
- `<style>` tags for CSS
- `<div>` tags for HTML structure
- `<script>` tags for JavaScript functionality

Simply edit the files to customize colors, animations, or behavior.

## 🚀 Performance Tips

1. **Use Production CDN**: raw.githack provides production-ready CDN links
2. **Lazy Load**: Load overlays only when needed
3. **Optimize Animations**: Reduce particle counts for slower devices
4. **Cache**: raw.githack automatically caches files for better performance

## 📱 Browser Compatibility

- ✅ Chrome/Edge (latest)
- ✅ Firefox (latest)
- ✅ Safari (latest)
- ✅ Mobile browsers

## 🤝 Contributing

Feel free to create new overlay themes and submit pull requests!

## 📄 License

Free to use for personal and commercial projects.

---

**Happy Coding! 🎉**