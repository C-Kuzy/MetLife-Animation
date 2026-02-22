# MetLife Banner Creation

An animated HTML banner generator for MetLife job offer announcements, featuring interactive particle effects and automated GIF conversion.

![MetLife Banner](https://img.shields.io/badge/MetLife-Banner-00A3E0?style=for-the-badge)
![License](https://img.shields.io/badge/License-EULA-blue?style=for-the-badge)

## 📋 Overview

This project creates professional, animated announcement banners for MetLife job offers and internships. The banner features MetLife's brand colors, interactive particle effects, and smooth animations that can be viewed in a browser or exported as a high-quality GIF.

**Creator:** Connor Kouznetsov (C-Kuzy)  
**Development Period:** January 10-15, 2026  
**Dimensions:** 1200x628px (optimized for LinkedIn/social media)

## ✨ Features

- **Interactive Particle System** - Dynamic particle network that responds to mouse movement
- **Smooth Animations** - Sliding geometric shapes with MetLife's signature blue and green colors
- **Customizable Content** - Easily update job title, location, program details, and hashtags
- **GIF Export** - Automated conversion to high-quality GIF format at 144 FPS
- **Ready for Deployment** - Pre-configured for Vercel deployment
- **Brand Accurate** - Uses MetLife's official branding and colors

## 🛠️ Technologies Used

### Frontend
- **HTML5** - Structure and layout
- **CSS3** - Animations and styling
- **JavaScript (ES6+)** - Particle system and canvas rendering
- **IBM Plex Sans** - Google Fonts (MetLife's brand font)

### Backend/Tools
- **Python 3** - GIF generation script
- **Playwright** - Headless browser automation for screenshot capture
- **Pillow (PIL)** - Image processing and GIF creation
- **Vercel** - Deployment platform

## 📦 Installation

### Prerequisites
- Python 3.8 or higher
- Node.js (optional, for local development server)

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/MetLife-Banner.git
   cd MetLife-Banner
   ```

2. **Install Python dependencies**
   ```bash
   pip install -r requirements_gif.txt
   ```

3. **Install Playwright browsers**
   ```bash
   playwright install chromium
   ```

## 🚀 Usage

### View the Banner Locally

Simply open `metlife_animated.html` in your web browser:

```bash
# Using Python's built-in server
python -m http.server 8000

# Then navigate to http://localhost:8000/metlife_animated.html
```

### Customize the Banner

Edit [`metlife_animated.html`](metlife_animated.html) to update:

```html
<div class="program-text">Tampa, FL</div>          <!-- Location -->
<h1>
    <span class="text-line">Summer 2026</span>     <!-- Season/Year -->
    <span class="text-line">Software Engineer</span> <!-- Job Title -->
</h1>
<div class="hashtag">#METxGlobalTechnologyProgram</div> <!-- Hashtag -->
```

### Generate GIF

Run the Python script to create an animated GIF:

```bash
python gif-conversion.py
```

**Configuration options** in `gif-conversion.py`:
- `fps` - Frame rate (default: 144)
- `duration` - Animation length in seconds (default: 1)
- `frame_delay_ms` - GIF playback speed (default: 32)
- `output_file` - Output filename

## 🎨 Customization

### Colors

MetLife brand colors are defined in [`style.css`](style.css):

```css
--metlife-blue: #00A3E0
--metlife-green: #7AB800
--metlife-navy: #002F6C
```

### Particle Effects

Modify particle settings in [`script.js`](script.js):

```javascript
this.particleCount = 80;           // Number of particles
this.connectionDistance = 150;      // Connection line distance
this.colors = [                     // Particle colors
    'rgba(0, 163, 224, 0.8)',
    'rgba(122, 184, 0, 0.8)',
    'rgba(255, 255, 255, 0.7)'
];
```

### Animation Timing

Adjust animation delays in [`style.css`](style.css):

```css
animation: slideIn 7.45s cubic-bezier(0.25, 0.46, 0.45, 0.94) forwards;
animation: slideIn 7.45s 2.45s cubic-bezier(0.25, 0.46, 0.45, 0.94) forwards;
```

## 🌐 Deployment

### Deploy to Vercel

1. Install Vercel CLI:
   ```bash
   npm i -g vercel
   ```

2. Deploy:
   ```bash
   vercel
   ```

The [`vercel.json`](vercel.json) configuration automatically redirects the root URL to the animated banner.

Alternatively, connect your GitHub repository to Vercel for automatic deployments on push.

## 📁 Project Structure

```
MetLife-Banner/
├── metlife_animated.html    # Main HTML banner
├── style.css                 # Styles and animations
├── script.js                 # Particle system logic
├── gif-conversion.py         # GIF generation script
├── requirements_gif.txt      # Python dependencies
├── vercel.json              # Vercel deployment config
├── EULA-LICENSE             # License agreement
├── README.md                # This file
└── temp/                    # Temporary files (gitignored)
```

## 📸 Output Examples

The banner displays:
- **MetLife Logo** with brand text
- **Location** (e.g., "Tampa, FL")
- **Position Details** (e.g., "Summer 2026 Software Engineer")
- **Program Hashtag** (e.g., "#METxGlobalTechnologyProgram")
- **Animated Background** with sliding blue and green shapes
- **Interactive Particles** that respond to mouse movement

## 🔧 Troubleshooting

### GIF Generation Issues

**Problem:** Playwright browser not found  
**Solution:** Run `playwright install chromium`

**Problem:** GIF file size too large  
**Solution:** Reduce `fps` or `duration` in `gif-conversion.py`

**Problem:** Animation not captured properly  
**Solution:** Increase the wait time in `page.wait_for_timeout(500)`

## 📄 License

This project is licensed under the C-Kuzy Solutions EULA. See [`EULA-LICENSE`](EULA-LICENSE) for full terms.

**Key Points:**
- Free to use, modify, and distribute (open-source and commercial)
- Attribution to Connor Kouznetsov (C-Kuzy Solutions) is required
- Source files must include proper headers

## 👤 Author

**Connor Kouznetsov (C-Kuzy)**
- GitHub: [@C-Kuzy](https://github.com/C-Kuzy)

## 🙏 Acknowledgments

- MetLife for brand assets and inspiration
- IBM Plex Sans font family
- Playwright and Pillow libraries

---

**Note:** This is a personal project created for job offer announcements. MetLife trademarks and branding are property of Metropolitan Life Insurance Company.