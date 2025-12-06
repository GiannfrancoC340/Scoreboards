# Soccer Scoreboard Project

## Project Overview
A responsive soccer scoreboard display built with HTML and CSS that shows the final score between Inter Miami CF and New York City FC on November 29, 2025. 
The project features team logos, scores, and styled gradient backgrounds for each team's section.

## Technologies Used
- HTML5
- CSS3 (Flexbox, Gradients)
- Web-safe fonts (Arial, Helvetica)

## Project Structure
```
├── index.html
└── styles.css
```

## Key Features

### 1. **Three-Section Layout**
The scoreboard is divided into three main sections:
- **Left Section**: Inter Miami (home team) - Pink/magenta gradient background
- **Middle Section**: Match status and statistics
- **Right Section**: New York City FC (away team) - Blue gradient background

### 2. **Responsive Container**
```css
.container {
    width: 100vw;  /* Full viewport width */
    height: 80vh;  /* 80% of viewport height */
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
}
```

### 3. **Gradient Backgrounds**
```css
.left {
    background: linear-gradient(135deg, #ff00ff, #ff69b4);
}

.right {
    background: linear-gradient(135deg, #0088ff, #00d4ff);
}
```

### 4. **Team Logos and Scores**
- Team logos displayed at 200x200px
- Large, bold score numbers (150px font size)
- Proper spacing using margin adjustments

## Design Decisions

### Layout Strategy
- Used **Flexbox** for the main container to create three equal sections
- Applied `flex: 1` to left and right sections to fill available space
- Set fixed width for middle section to maintain consistent spacing

### Spacing Solution
**Problem**: Logo and score were too far apart initially due to `margin-top: 80px`

**Solution**: Changed to `margin-bottom: 10px` to create proper spacing between logo and score while keeping them close together.

### Edge-to-Edge Layout
**Problem**: Default browser margins created unwanted whitespace

**Solution**:
```css
body {
    margin: 0;
    padding: 0;
}
```

### Gradient Background Implementation
Used `linear-gradient()` with 135-degree angle to create diagonal gradients that add visual appeal without overwhelming the content.

## Color Scheme
- **Inter Miami**: Pink/Magenta gradient (#ff00ff → #ff69b4)
- **NYC FC**: Blue gradient (#0088ff → #00d4ff)
- **Scores**: Black for home team, RGB blue (0, 136, 255) for away team
- **Status Text**: Black on light background

## Typography
- **Font Family**: Arial, Helvetica, sans-serif (web-safe fonts)
- **Score Size**: 150px (bold, high visibility)
- **Status Text**: 50px for "Full Time"
- **Font Weight**: Lighter weight for scores to maintain clean aesthetic

## Lessons Learned

### 1. **Margin vs. Padding**
Understanding when to use margin vs. padding for spacing:
- `margin-top` pushes elements down from their container
- `margin-bottom` creates space below elements without affecting vertical centering

### 2. **Flexbox Alignment**
- `justify-content: space-evenly` - distributes items with equal space
- `align-items: center` - vertically centers items
- `flex: 1` - allows sections to grow and fill space

### 3. **Viewport Units**
- `100vw` ensures full width regardless of screen size
- `80vh` creates consistent height relative to viewport

### 4. **Border Removal**
Removing default body margins is essential for edge-to-edge layouts in modern web design.

## Future Enhancements
Potential additions to consider:
- Add statistics section in the middle (shots, possession, etc.)
- Include match date/time information
- Add animations for score updates
- Make responsive for mobile devices
- Include player statistics or key events

## File Reference

### HTML Structure
```html
<div class="container">
    <div class="left">
        <img class="item" src="[Inter Miami Logo]">
        <h1 class="home-score">5</h1>
    </div>
    <div class="middle">
        <h2>Full Time</h2>
    </div>
    <div class="right">
        <img class="item" src="[NYC FC Logo]">
        <h1 class="away-score">1</h1>
    </div>
</div>
```

### CSS Highlights
- Flexbox for layout control
- Linear gradients for visual appeal
- Web-safe fonts for compatibility
- Viewport units for responsiveness

## Takeaways
This project demonstrates:
- ✅ Clean, semantic HTML structure
- ✅ Modern CSS layout techniques (Flexbox)
- ✅ Effective use of gradients and colors
- ✅ Proper spacing and alignment
- ✅ Responsive design principles

The scoreboard successfully displays match information in a visually appealing and well-organized format, with clear team branding through colors and logos.

