# Customization Guide - Nail Beautiful Blogger Template

Professional customization guide to personalize your Blogger template to match your exact brand.

---

## 🎨 Color System Customization

### Primary Colors (Main Brand Color)

The main color used for buttons, links, and accents.

**Current:** Luxury Rose (`#d87a7a`)

**To Change:**

1. Go to **Theme** → **Edit HTML**
2. Find (around line 23):
```css
:root {
  --primary: #d87a7a;
  --primary-dark: #b75d63;
```

3. Replace `#d87a7a` with your color

**Recommended Colors for Nail Niche:**

| Theme | Primary | Dark | Accent |
|-------|---------|------|--------|
| Rose Gold | `#d87a7a` | `#b75d63` | `#f1c7be` |
| Coral Blush | `#ff6b6b` | `#cc5555` | `#ffc3c3` |
| Grape Luxe | `#8b5a8e` | `#6b4470` | `#d4b5d4` |
| Peach Dream | `#f89b7b` | `#d67a5c` | `#ffc4a3` |
| Nude Elegance | `#d4a5a5` | `#b08080` | `#e8cfc9` |

### Complete Color Variables

```css
:root {
  --bg: #f9f4f2;                    /* Page background */
  --panel: #fffdfc;                 /* Card/panel background */
  --panel-strong: #ffffff;          /* Strong panel (white) */
  --primary: #d87a7a;               /* Main brand color */
  --primary-dark: #b75d63;          /* Hover/dark version */
  --secondary: #f1c7be;             /* Accent color */
  --soft: #f4e0d8;                  /* Light background */
  --dark: #2f2a2b;                  /* Text color (dark) */
  --muted: #6f6467;                 /* Secondary text */
  --line: rgba(47,42,43,.12);       /* Borders */
  --shadow: 0 18px 45px rgba(68, 44, 44, 0.08); /* Shadows */
  --radius: 22px;                   /* Border radius */
}
```

**Complete Example - Change to Coral:**

```css
:root {
  --bg: #fff5f3;                    /* Light coral background */
  --panel: #fffdfc;
  --panel-strong: #ffffff;
  --primary: #ff6b6b;               /* Coral main */
  --primary-dark: #cc5555;          /* Darker coral */
  --secondary: #ffc3c3;             /* Light coral */
  --soft: #ffe8e8;
  --dark: #2f2a2b;
  --muted: #6f6467;
  --line: rgba(255,107,107,.12);
  --shadow: 0 18px 45px rgba(255, 107, 107, 0.08);
  --radius: 22px;
}
```

---

## 🔤 Typography Customization

### Change Fonts

The template uses Google Fonts:
- **Headlines:** Cormorant Garamond (elegant serif)
- **Body:** Poppins (modern sans-serif)

**To Change Fonts:**

1. Go to **Theme** → **Edit HTML**
2. Find (around line 20):
```xml
<link href='https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@500;600;700&amp;family=Poppins:wght@400;500;600;700&amp;display=swap' rel='stylesheet'/>
```

3. Visit https://fonts.google.com
4. Select new fonts
5. Copy the link and replace

**Popular Font Combinations:**

| Style | Headline | Body |
|-------|----------|------|
| Luxury | Cormorant Garamond | Poppins |
| Modern | Playfair Display | Inter |
| Elegant | Montserrat | Open Sans |
| Creative | Raleway | Lato |

### Adjust Font Sizes

Find and modify these in CSS:

```css
h1 { font-size: 3rem; }           /* Large headings */
h2 { font-size: 2.2rem; }         /* Article titles */
h3 { font-size: 1.8rem; }         /* Section titles */
.post-title a { font-size: clamp(2rem, 2.4vw, 3rem); }
```

---

## 🖼️ Logo & Header Customization

### Replace Logo (Easy Way)

1. Go to **Layout**
2. Find **Header** widget
3. Click **Edit**
4. Upload your logo image
5. Adjust size: 300x100px or 400x150px recommended

### Logo Dimensions

| Use Case | Width | Height |
|----------|-------|--------|
| Small (sticky header) | 200px | 60px |
| Medium | 300px | 100px |
| Large (desktop) | 400px | 150px |

### Header Background Customization

To change the header background color:

1. Find in CSS (around line 80):
```css
.header-wrap {
  background: rgba(255,255,255,.7);
  backdrop-filter: blur(12px);
}
```

2. Replace `rgba(255,255,255,.7)` with your color:
   - `rgba(255,255,255,.7)` = White with 70% opacity
   - `rgba(216,122,122,.9)` = Rose with 90% opacity

---

## 🌐 Navigation Menu Customization

### Change Menu Items

Find the navigation menu (around line 380):

```xml
<ul class='main-nav'>
  <li><a href='/'>Home</a></li>
  <li><a href='/search/label/Nail%20Polish'>Nail Polish</a></li>
  <li><a href='/search/label/Acrylic%20Nails'>Acrylic Nails</a></li>
  <li><a href='/search/label/Neon%20Nails'>Neon Nails</a></li>
  <li><a href='/search/label/Spring%20Nails'>Spring Nails</a></li>
  <li><a href='/search/label/Gel%20Manicure'>Gel Manicure</a></li>
  <li><a href='/p/contact-us.html'>Contact</a></li>
</ul>
```

### Replace with Your Categories

**Example 1: More specific nail styles**
```xml
<ul class='main-nav'>
  <li><a href='/'>Home</a></li>
  <li><a href='/search/label/French%20Nails'>French Nails</a></li>
  <li><a href='/search/label/Ombre%20Nails'>Ombre Nails</a></li>
  <li><a href='/search/label/3D%20Nails'>3D Nails</a></li>
  <li><a href='/search/label/Minimalist%20Nails'>Minimalist</a></li>
  <li><a href='/search/label/Nail%20Care'>Care &amp; Tips</a></li>
  <li><a href='/p/contact.html'>Contact</a></li>
</ul>
```

**Example 2: General beauty**
```xml
<ul class='main-nav'>
  <li><a href='/'>Home</a></li>
  <li><a href='/search/label/Nails'>Nails</a></li>
  <li><a href='/search/label/Makeup'>Makeup</a></li>
  <li><a href='/search/label/Hair'>Hair</a></li>
  <li><a href='/search/label/Skincare'>Skincare</a></li>
  <li><a href='/p/shop.html'>Shop</a></li>
</ul>
```

### Add Dropdown Menus

To add submenus under items:

```xml
<li>
  <a href='/search/label/Nail%20Styles'>Nail Styles</a>
  <ul class='submenu'>
    <li><a href='/search/label/Acrylic'>Acrylic</a></li>
    <li><a href='/search/label/Gel'>Gel</a></li>
    <li><a href='/search/label/Natural'>Natural</a></li>
  </ul>
</li>
```

---

## 🎯 Featured Section Customization

### Change Featured Images

Find the featured strip (around line 430):

```xml
<article class='featured-item'>
  <img alt='Featured nail design' src='https://images.unsplash.com/photo-1522335789203-aabd1fc54bc9?auto=format&amp;fit=crop&amp;w=900&amp;q=80'/>
  <div class='meta'><a href='/search/label/Nail%20Designs'>Nail Art Ideas</a></div>
</article>
```

**Replace the URL** with your image:
- Use your own image URL (Unsplash, Pexels, or uploaded to Blogger)
- Keep image size: 900x220px for best results

**Free Image Sources:**
- Unsplash.com
- Pexels.com
- Pixabay.com
- Your own photography

### Featured Section CSS

Adjust featured item height:

```css
.featured-item img {
  height: 220px;  /* Change this value */
  object-fit: cover;
}

@media (max-width: 640px) {
  .featured-item img {
    height: 180px;  /* Mobile height */
  }
}
```

---

## 📱 Mobile Customization

### Adjust Mobile Breakpoints

Change when design switches to mobile:

```css
@media (max-width: 980px) {
  /* Tablet and smaller */
}

@media (max-width: 760px) {
  /* Mobile phones */
}

@media (max-width: 640px) {
  /* Small phones */
}
```

### Mobile Menu Button Style

Customize the hamburger menu:

```css
.mobile-toggle {
  width: 42px;           /* Button size */
  height: 42px;
  background: #fff;      /* Background color */
  border: 1px solid var(--line);
  color: var(--dark);
  cursor: pointer;
}
```

### Adjust Sidebar on Mobile

The sidebar moves below posts on mobile. To change:

```css
.page-shell {
  display: grid;
  grid-template-columns: minmax(0, 2.2fr) minmax(300px, .9fr);
  gap: 28px;
}

@media (max-width: 980px) {
  .page-shell {
    grid-template-columns: 1fr;  /* Single column on mobile */
  }
}
```

---

## 🎨 Button & Link Customization

### Change Button Colors

Find button styles:

```css
.header-button {
  background: var(--primary);        /* Normal state */
}

.header-button:hover {
  background: var(--primary-dark);   /* Hover state */
}
```

### Change Link Colors

```css
a {
  color: var(--primary-dark);        /* Link color */
}

a:hover {
  color: var(--primary);             /* Hover color */
}
```

---

## 🔘 Widget Customization

### Add Custom Widgets

Go to **Layout** and add:

1. **Popular Posts** - Most viewed articles
2. **Labels** - Category cloud
3. **Recent Posts** - Latest articles
4. **Newsletter** - Email signup
5. **Social Links** - Follow buttons
6. **Custom HTML** - Ads or custom content

### Newsletter Widget

Edit in **Layout** → **Newsletter widget**:

```xml
<h2>Join the Beauty List</h2>
<p>Get weekly nail inspiration and beauty tips</p>
<form>
  <input placeholder='Your email' type='email'/>
  <button>Subscribe</button>
</form>
```

### Social Links Widget

Go to **Layout** and add social links:
- Facebook
- Instagram
- Pinterest
- TikTok
- YouTube

---

## 📐 Spacing & Layout Customization

### Adjust Post Spacing

```css
.post {
  margin-bottom: 26px;      /* Space between posts */
  border-radius: var(--radius);
  padding: 20px;            /* Internal padding */
}
```

### Adjust Sidebar Spacing

```css
.page-shell {
  gap: 28px;  /* Space between content and sidebar */
}
```

### Adjust Widget Spacing

```css
.widget {
  margin-bottom: 24px;      /* Space between widgets */
  padding: 20px 18px;       /* Internal padding */
}
```

---

## 🔍 Advanced CSS Customization

### Rounded Corners

All rounded elements use `--radius: 22px`. To change:

```css
:root {
  --radius: 22px;    /* Default: very rounded */
  --radius: 12px;    /* More subtle */
  --radius: 4px;     /* Sharp corners */
}
```

### Box Shadows

Current shadow style:

```css
--shadow: 0 18px 45px rgba(68, 44, 44, 0.08);
```

Make more dramatic:

```css
--shadow: 0 20px 60px rgba(68, 44, 44, 0.15);
```

Make subtle:

```css
--shadow: 0 4px 12px rgba(68, 44, 44, 0.05);
```

---

## 🌍 Multi-Language Customization

### English (Default)

No changes needed - template is in English.

### Change Button Text

Find text in HTML (around line 370):

```xml
<button class='header-button' type='button'>Newsletter</button>
```

Replace with your text or translate to another language.

### Change Placeholder Text

```xml
<input placeholder='Search trends...' type='search'/>
```

Change `'Search trends...'` to any language.

### Common Translations

| Text | Spanish | French |
|------|---------|--------|
| Home | Inicio | Accueil |
| Search | Buscar | Rechercher |
| Newsletter | Boletín | Infolettre |
| Categories | Categorías | Catégories |
| Follow Us | Síguenos | Suivez-nous |

---

## 🔧 Common Customizations Checklist

- [ ] Change primary color
- [ ] Update logo
- [ ] Change navigation menu
- [ ] Update blog title and description
- [ ] Customize featured images
- [ ] Adjust font sizes
- [ ] Change footer information
- [ ] Add social media links
- [ ] Set up newsletter
- [ ] Configure AdSense placements
- [ ] Test on mobile
- [ ] Verify all links work

---

## ✅ Testing Your Customizations

After making changes:

1. **Clear browser cache** (Ctrl+Shift+Delete)
2. **Wait 2-5 minutes** for Blogger to update
3. **Test on desktop** (Chrome, Firefox, Safari, Edge)
4. **Test on mobile** (iOS and Android)
5. **Check all links** work correctly
6. **Verify images** load properly

---

## 🆘 Troubleshooting Customizations

### Changes Don't Appear

- Clear browser cache and cookies
- Wait 5 minutes for Blogger to update
- Try incognito/private browsing mode
- Try different browser

### Layout Breaks

- Check for missing closing tags `</>`
- Verify all quotes are properly closed `"` or `'`
- Don't delete important CSS rules
- Use original template as reference

### Mobile View Issues

- Test in Chrome DevTools mobile mode
- Check media queries (max-width breakpoints)
- Verify touch targets are large enough
- Test on actual mobile devices

---

**Happy Customizing!** 🎉

Your Nail Beautiful template is now fully personalized to match your unique brand style.

For support or advanced modifications, refer to the main README.md or visit your Blogger dashboard settings.
