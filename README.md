
# Parallax Background Component

A reusable JavaScript component that creates a 4-row scrolling parallax background.

## Quick Start

### Method 1: Simple Integration
```html
<script src="parallax-bg.js"></script>
<script>
  ParallaxBackground.init({
    zIndex: -1,
    speeds: [50, 70, 42, 20]
  });
</script>
```

### Method 2: Auto-initialization
```html
<script src="parallax-bg.js" 
        data-auto-init 
        data-z-index="-1"></script>
```

## Demo

1. **Install dependencies:**
   ```bash
   npm install
   ```

2. **Start the server:**
   ```bash
   npm start
   ```

3. **View demos:**
   - Main parallax demo: [http://localhost:3000](http://localhost:3000)
   - Login page with parallax background: [http://localhost:3000/test.html](http://localhost:3000/test.html)

## Configuration Options

```javascript
ParallaxBackground.init({
  containerSelector: "body",           // Target container
  zIndex: -1,                         // Background layer depth
  speeds: [50, 70, 42, 20],          // Animation speeds for each row (seconds)
  gap: "8px",                        // Gap between images
  imagesPerRow: 6,                   // Number of images per row
  imageUrls: [/* custom URLs */]     // Override default Cloudinary images
});
```

## Image Optimization

Images are served via Cloudinary with advanced optimizations:
- **Size**: Resized to max 500px width (`w_500,c_limit`)
- **Quality**: Automatic quality optimization (`q_auto:low`)
- **Format**: Auto-format selection for modern browsers (`f_auto`)
- **Loading**: Progressive JPEG delivery (`fl_progressive`)

## API Methods

- `ParallaxBackground.init(options)` - Initialize with options
- `instance.destroy()` - Remove parallax background and cleanup

## Browser Support

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers with CSS animation support