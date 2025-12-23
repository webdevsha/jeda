# Jeda | The Sovereign Architect's Lab

![Jeda](https://ik.imagekit.io/cbctech/Gemini_Generated_Image_17dvmp17dvmp17dv.png?updatedAt=1766390152502)

**Pause Daily. Build Slowly.** - A digital garden exploring the intersection of philosophy, mathematics, AI sovereignty, and community-driven learning.

---

## 🌿 Philosophy

**Jeda** (Indonesian/Malay: *pause, break, rest*) is a personal laboratory and collective space for architects of sovereign systems. It's built on the principle that meaningful technology emerges from intentional pauses—moments of reflection before creation.

### Core Pillars

```
The Soul → The Logic → The Lab → The Hands → The Library → The Collective
```

---

## ✨ Overview

Jeda is an interactive, cork-board-style landing page that visualizes a multi-layered personal curriculum through scattered "sticky notes." Each note represents a domain of study and practice, creating a holistic approach to building sovereign technology.

### The Garden Board Metaphor
- **Visual**: Scattered sticky notes on a textured background (like a bulletin board)
- **Interactive**: Clickable notes reveal deeper context via modals
- **Organic**: Parallax mouse effects make notes feel "floating" in space
- **Responsive**: Transforms from scattered layout to organized grid on mobile

---

## 🎯 The Six Domains

### 1. **Al-Ghazali** (The Theory)
- **Focus**: Internal spiritual architecture
- **Color**: Olive green
- **Content**: Studying *Ihya Ulumuddin* - the purification of intention (niat) and heart as prerequisites for building technology
- **Position**: Top-left

### 2. **Polya's Math** (The Logic)
- **Focus**: Problem-solving heuristics and mathematical beauty
- **Color**: White/Paper
- **Content**: Reading *How to Solve It* by G. Polya - understanding problem structure before coding
- **Position**: Top-right

### 3. **The AI Equation** (The Lab)
- **Focus**: Local AI, privacy, and computational sovereignty
- **Color**: Cherry red
- **Content**: Researching local LLMs, alignment, robustness, and building Family-CommunityAI
- **Position**: Bottom-left

### 4. **The Box** (The Hands)
- **Focus**: Physical prototyping and tangible creations
- **Color**: Mustard yellow
- **Content**: Projects like Ocean Weight Dumbbells (recycled plastic) and Jeda Candle Timer
- **Position**: Bottom-right

### 5. **Articles** (The Library)
- **Focus**: Curated reading and research
- **Color**: White/Paper
- **Content**: Papers on biomimicry, gift economy (Charles Eisenstein), digital minimalism
- **Position**: Middle-left

### 6. **The Village** (The Collective)
- **Focus**: Community learning and shared curriculum
- **Color**: Olive green
- **Content**: Monthly gatherings to share personal curriculums and build together
- **Position**: Middle-right

---

## 🛠️ Technical Features

### Design System

**Color Palette:**
```css
--bg-garden: #F3F5EE    /* Soft off-white green background */
--mustard: #E6C229       /* Warm yellow accent */
--olive: #8A9A5B         /* Natural green */
--cherry: #D9534F        /* Bold red */
--paper: #FFFCF5         /* Cream white */
--ink: #2C3E50           /* Dark blue-gray text */
```

**Typography:**
- **Display**: La Belle Aurore (cursive, handwritten feel)
- **Body**: DM Sans (clean, modern sans-serif)
- Mix of elegance and readability

### Interactive Elements

#### 1. **Sticky Note System**
```html
<div class="note [color] [position]" onclick="openModal(...)">
  <h3>Title</h3>
  <p>Brief description</p>
  <div class="note-footer">Category</div>
</div>
```

**Features:**
- Pseudo-element "tape" effect at the top
- Hover state: scales and straightens (removes rotation)
- Click: opens detailed modal
- Initial rotation for organic feel

#### 2. **Parallax Mouse Tracking**
```javascript
document.addEventListener('mousemove', (e) => {
  // Calculates subtle drift based on mouse position
  // Different speeds per note for depth perception
  // Disabled on mobile for performance
});
```

#### 3. **Modal Information System**
```javascript
function openModal(title, desc, content) {
  // Populates and displays modal overlay
  // Backdrop blur + smooth animations
}
```

### Responsive Design

**Desktop (>900px):**
- Notes positioned absolutely with rotation
- Parallax mouse effects active
- Center title with scattered notes around it

**Mobile (≤900px):**
- Notes become relative-flow grid layout
- 2-column arrangement (140px notes)
- Alternating rotations for visual interest
- Parallax disabled for performance
- Vertical scroll through content

---

## 🚀 Getting Started

### Installation

1. **Download** the HTML file
2. **No dependencies** - pure HTML/CSS/JS
3. **Open** in any modern browser
4. **Optional**: Host on static site (Netlify, Vercel, GitHub Pages)

### Quick Deploy

**GitHub Pages:**
```bash
git init
git add index.html
git commit -m "Initial commit: Jeda landing page"
git branch -M main
git remote add origin [your-repo-url]
git push -u origin main
```

Enable GitHub Pages in repository settings → select `main` branch.

**Netlify Drop:**
Simply drag the HTML file into Netlify's drag-and-drop interface.

---

## 🎨 Customization Guide

### Adding New Notes

```html
<div class="note [color] pos-[n]" onclick="openModal('Title', 'Subtitle', 'Full description')">
    <h3>Note Title</h3>
    <p>Brief teaser text</p>
    <div class="note-footer">Category Label</div>
</div>
```

**Available Colors:**
- `mustard` - Yellow background
- `olive` - Green background (white text)
- `cherry` - Red background (white text)
- `white` - Default cream paper color

### Positioning System (Desktop)

Create new position classes:
```css
.pos-7 { 
  top: 30%; 
  left: 50%; 
  transform: translateX(-50%) rotate(-3deg); 
}
```

**Tips:**
- Use percentages for responsive positioning
- Rotate between -8deg and 8deg for natural look
- Avoid overlap with center title area

### Changing Brand Colors

Update CSS variables in `:root`:
```css
:root {
  --bg-garden: #F3F5EE;  /* Background */
  --mustard: #E6C229;     /* Primary CTA */
  --olive: #8A9A5B;       /* Secondary accents */
  --cherry: #D9534F;      /* Urgent/important */
}
```

### Updating Content

**Hero Title:**
```html
<h1>Jeda</h1>
<p>Pause Daily. Build Slowly.</p>
```

**Doodle/Logo:**
```html
<img src="[your-image-url]" alt="Brand Doodle" class="doodle-img">
```

**Call-to-Action Buttons:**
```html
<a href="[your-link]" class="btn btn-primary">Button Text</a>
```

---

## 📱 Mobile Experience

### Layout Transformation

**Desktop View:**
```
        [Note 5]    [JEDA]    [Note 2]
                     TITLE
        [Note 1]              [Note 6]
        
        [Note 3]              [Note 4]
```

**Mobile View:**
```
    [JEDA TITLE]
    
    [Note] [Note]
    [Note] [Note]
    [Note] [Note]
    
    [CTA Buttons]
```

### Performance Optimizations

- Parallax disabled on mobile
- Smaller note sizes (140px vs 180px)
- Relative positioning for smoother scrolling
- Reduced shadow complexity

---

## 🎭 Modal System

### Structure

```html
<div class="modal-overlay" id="infoModal">
  <div class="modal-content">
    <h2 id="modalTitle">Title</h2>
    <p id="modalDesc">Description</p>
    <p id="modalContent">Full content</p>
  </div>
</div>
```

### Usage

```javascript
openModal(
  'Topic Name',           // Main title
  'Brief description',    // Subtitle/context
  'Full detailed content' // Body text
);
```

### Styling

- Backdrop blur for depth
- Smooth cubic-bezier animations
- Center-aligned content
- Click outside to close

---

## 🌐 Browser Compatibility

- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

**CSS Features Used:**
- CSS Grid & Flexbox
- CSS Variables (Custom Properties)
- Backdrop-filter (with fallback)
- Transform & Transitions

---

## 🎓 Educational Use Cases

### Personal Portfolio
- Showcase multi-disciplinary interests
- Visual curriculum vitae
- Interactive project showcase

### Learning Journal
- Document reading lists
- Track research domains
- Share progress with mentors

### Community Platform
- Collective knowledge mapping
- Shared curriculum template
- Workshop/course landing page

---

## 🔧 Advanced Customization

### Adding Background Patterns

Current pattern:
```css
background-image: radial-gradient(var(--olive) 0.5px, transparent 0.5px);
background-size: 20px 20px;
```

**Alternative patterns:**
- Grid: `linear-gradient()`
- Noise: Use SVG filter
- Texture: Add subtle image overlay

### Animation Enhancements

**Note entrance animations:**
```css
@keyframes noteAppear {
  from { 
    opacity: 0; 
    transform: translateY(20px) rotate(0deg); 
  }
  to { 
    opacity: 1; 
    transform: translateY(0) rotate(var(--note-rotation)); 
  }
}

.note {
  animation: noteAppear 0.6s cubic-bezier(0.34, 1.56, 0.64, 1);
  animation-delay: calc(var(--note-index) * 0.1s);
}
```

### Dark Mode Support

```css
@media (prefers-color-scheme: dark) {
  :root {
    --bg-garden: #1a1f1a;
    --paper: #2a2f2a;
    --ink: #e8e8e8;
  }
}
```

---

## 📚 Philosophical Foundations

### The Three Layers of Study

**Layer 1: Theory (The Soul)**
- Philosophical foundations
- Ethical frameworks
- Intentionality and purpose

**Layer 2: Logic (The Mind)**
- Mathematical structures
- Problem-solving heuristics
- System thinking

**Layer 3: Praxis (The Hands)**
- Technical implementation
- Physical prototyping
- Community building

### Inspired By

- **Al-Ghazali**: Islamic philosophy and spiritual purification
- **G. Polya**: Mathematical problem-solving and heuristics
- **Charles Eisenstein**: Gift economy and sacred economics
- **Cal Newport**: Digital minimalism and deep work
- **Janine Benyus**: Biomimicry and nature-inspired design

---

## 🚧 Roadmap & Future Enhancements

### Planned Features
- [ ] Blog/article integration
- [ ] Curriculum submission form (Airtable/Google Forms)
- [ ] Dark mode toggle
- [ ] Reading list database
- [ ] Project portfolio gallery
- [ ] Community forum/discussion board
- [ ] Newsletter signup
- [ ] Multi-language support (EN/MS/ID)

### Technical Improvements
- [ ] Add meta tags for SEO
- [ ] Implement proper analytics (privacy-focused)
- [ ] Add RSS feed for updates
- [ ] Create JSON data structure for notes (easier updates)
- [ ] Accessibility improvements (ARIA labels, keyboard nav)
- [ ] Progressive Web App (PWA) capabilities

---

## 🤝 Contributing

This is a personal project template, but feel free to:
- Fork and adapt for your own curriculum
- Share improvements via pull requests
- Suggest features via issues
- Use as inspiration for your digital garden

### Adaptation Guidelines

When using this template:
1. Replace content with your own domains of study
2. Update colors to match your aesthetic
3. Change the doodle/logo to your brand
4. Modify the tagline to reflect your philosophy
5. Credit inspiration if sharing publicly

---

## 📄 License

This template is provided as-is for educational and personal use.

**Attribution Appreciated:**
"Inspired by Jeda - The Sovereign Architect's Lab"

---

## 📞 Connect

- **Concept**: Personal curriculum & digital garden
- **Philosophy**: Slow tech, intentional building, community learning
- **Instagram**: [Update with your handle]
- **Community**: "The Jeda Collective" - monthly gatherings

---

## 🎨 Design Credits

- **Typography**: 
  - La Belle Aurore by [Designer Name]
  - DM Sans by Colophon Foundry
- **Color Palette**: Custom "Garden Study" theme
- **Iconography**: Custom SVG icons
- **Image**: ImageKit CDN

---

## 💡 Usage Tips

### For Personal Use
1. Update each note with your current studies
2. Link to actual resources (books, papers, projects)
3. Keep modal content concise but meaningful
4. Update quarterly to reflect learning journey

### For Community/Workshop
1. Make notes represent workshop modules
2. Add registration form to CTA
3. Include facilitator bios in modals
4. Create shareable graphics from the layout

### For Portfolio
1. Replace domains with project categories
2. Link notes to case studies
3. Add "Work with me" CTA
4. Include contact form

---

## 🌟 Key Differentiators

**Why Jeda Stands Out:**
- ✨ Non-linear navigation (exploration over prescription)
- 🎨 Organic, hand-crafted aesthetic (anti-corporate)
- 🧠 Multi-disciplinary integration (soul + logic + praxis)
- 🤝 Community-first approach (collective learning)
- 🐌 Slow tech philosophy (pause before building)

---

**Built with intention. Shared with care. Evolved through community.**

*"The best technology emerges from a well-cultivated soul."*
