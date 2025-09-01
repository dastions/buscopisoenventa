# Background Image Setup

## 🖼️ **Hero Section Background**

### **Current Implementation:**
- **File**: `hero-background.svg`
- **Type**: SVG pattern with Spanish architecture elements
- **Size**: 7.5KB (optimized)
- **Features**: 
  - Spanish building silhouettes
  - Windows and balconies
  - Gradient overlays
  - Responsive design

### **CSS Structure:**
```css
.hero {
  /* Base gradient */
  background: linear-gradient(135deg, 
    rgba(102, 126, 234, 0.8) 0%, 
    rgba(118, 75, 162, 0.8) 50%, 
    rgba(44, 62, 80, 0.9) 100%);
}

.hero::before {
  /* SVG background pattern */
  background-image: url('/assets/hero-background.svg');
  opacity: 0.4;
  z-index: -2;
}

.hero::after {
  /* Gradient overlay for text readability */
  background: linear-gradient(135deg, 
    rgba(102, 126, 234, 0.7) 0%, 
    rgba(118, 75, 162, 0.7) 50%, 
    rgba(44, 62, 80, 0.8) 100%);
  z-index: -1;
}
```

### **Benefits:**
✅ **No external dependencies** - SVG is embedded  
✅ **Fast loading** - Only 7.5KB  
✅ **Scalable** - Vector graphics  
✅ **Spanish theme** - Architecture elements  
✅ **Professional look** - Modern design  
✅ **Text readable** - Proper contrast  

### **Customization Options:**

#### **1. Change Colors:**
Edit the SVG file to modify building colors and gradients.

#### **2. Adjust Opacity:**
```css
.hero::before {
  opacity: 0.3; /* More subtle */
  /* or */
  opacity: 0.6; /* More prominent */
}
```

#### **3. Replace with Photo:**
```css
.hero::before {
  background-image: url('/assets/your-photo.jpg');
}
```

#### **4. Add Animation:**
```css
.hero::before {
  animation: slowPan 20s infinite linear;
}

@keyframes slowPan {
  0% { background-position: 0% 50%; }
  100% { background-position: 100% 50%; }
}
```

### **Mobile Optimization:**
- `background-attachment: scroll` on mobile devices
- Responsive SVG viewBox
- Optimized for all screen sizes

---

**Status**: ✅ **Active and working**
**Last Updated**: Current implementation
