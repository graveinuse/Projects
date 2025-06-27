# 🧮 Web-Based Python Calculator

![Calculator Banner](./images/web-calculator-banner.png)

A modern, responsive web-based calculator built with HTML, CSS, and JavaScript. This calculator provides a sleek interface for basic arithmetic operations and mathematical functions, accessible from any web browser.

## ✨ Features

- **Basic Operations**: Addition (+), Subtraction (-), Multiplication (*), Division (/)
- **Advanced Functions**: Square root (√), Sign toggle (±)
- **Modern UI**: Beautiful gradient background with color-coded buttons
- **Responsive Design**: Works perfectly on desktop, tablet, and mobile devices
- **Keyboard Support**: Full keyboard input functionality
- **Error Handling**: Comprehensive error management for invalid operations
- **Visual Feedback**: Hover effects and smooth animations
- **Cross-Platform**: Runs in any modern web browser

![Main Interface](./images/web-calculator-main.png)
*Modern web interface with gradient background and intuitive button layout*

## 🚀 Getting Started

### Prerequisites

- Any modern web browser (Chrome, Firefox, Safari, Edge)
- Python 3.x (for local server hosting - optional)

### Quick Start

**Method 1: Direct File Opening**
1. Download or clone the repository
2. Double-click `calculator.html` to open in your default browser
3. Start calculating immediately!

**Method 2: Local Server (Recommended)**
```bash
# Clone the repository
git clone https://github.com/yourusername/web-calculator.git
cd web-calculator

# Start a local server
python -m http.server 8000

# Open in browser
# Navigate to http://localhost:8000/calculator.html
```

**Method 3: GitHub Codespaces/GitPod**
```bash
# In your codespace terminal
python -m http.server 8000

# Use the port forwarding feature to access the calculator
```

## 🎯 Usage

### Basic Operations
1. **Number Input**: Click number buttons (0-9) or use keyboard
2. **Decimal Point**: Click the decimal button (.) or press period key
3. **Operations**: Click operator buttons (+, -, *, /) or use keyboard
4. **Calculate**: Click equals (=) button or press Enter key

![Basic Calculation](./images/basic-calculation-web.png)
*Example of performing basic arithmetic: 15.5 + 24.3 = 39.8*

### Advanced Functions
- **Square Root (√)**: Click the √ button after entering a number
- **Sign Toggle (±)**: Change positive/negative sign of current number
- **Clear All (C)**: Clear the entire display (or press Escape/C)
- **Clear Entry (CE)**: Remove the last entered digit (or press Backspace)

![Advanced Functions](./images/advanced-functions-web.png)
*Demonstrating square root calculation: √64 = 8*

### Keyboard Shortcuts
| Key | Function |
|-----|----------|
| `0-9` | Number input |
| `.` | Decimal point |
| `+ - * /` | Basic operators |
| `Enter` or `=` | Calculate result |
| `Escape` or `C` | Clear all |
| `Backspace` | Clear last entry |

## 🏗️ Project Structure

```
web-calculator/
│
├── calculator.html           # Main application file (HTML + CSS + JS)
├── README.md                # Project documentation
├── requirements.txt         # Server dependencies (optional)
├── images/                  # Screenshots and assets
│   ├── web-calculator-banner.png
│   ├── web-calculator-main.png
│   ├── basic-calculation-web.png
│   ├── advanced-functions-web.png
│   └── error-handling-web.png
├── assets/                  # Additional resources (optional)
│   └── favicon.ico
└── docs/                    # Additional documentation
    └── deployment-guide.md
```

## 🎨 Design Features

### Visual Design
- **Modern Gradient Background**: Beautiful purple-blue gradient
- **Glass-morphism Effect**: Semi-transparent calculator body with blur effects
- **Color-Coded Buttons**:
  - 🔵 Blue: Special functions (Clear, Square root)
  - 🟠 Orange: Basic operators (+, -, *, /)
  - 🟢 Green: Equals button
  - ⚪ Light gray: Numbers and decimal point
- **Smooth Animations**: Hover effects and button press feedback
- **Typography**: Clean, bold fonts optimized for readability

### Responsive Design
- **Mobile-First Approach**: Optimized for touch interfaces
- **Flexible Grid Layout**: Adapts to different screen sizes
- **Touch-Friendly Buttons**: Large button sizes for easy tapping
- **Viewport Optimization**: Perfect scaling on all devices

![Mobile View](./images/mobile-calculator.png)
*Calculator optimized for mobile devices*

## ⚡ Technical Implementation

### HTML Structure
- Semantic HTML5 elements
- Accessible button markup with proper ARIA labels
- Clean, organized structure

### CSS Features
- **CSS Grid**: Modern layout system for button arrangement
- **Flexbox**: Flexible display alignment
- **CSS Variables**: Consistent color theming
- **Media Queries**: Responsive breakpoints
- **Transitions**: Smooth hover and click animations

### JavaScript Functionality
- **Event Handling**: Click and keyboard event listeners
- **Expression Evaluation**: Safe mathematical expression parsing
- **Error Management**: Robust error handling with user-friendly messages
- **State Management**: Proper calculator state handling
- **Input Validation**: Prevents invalid operations

```javascript
// Example of core calculation function
function calculate() {
    try {
        let expression = currentInput.replace(/×/g, '*').replace(/÷/g, '/');
        let result = eval(expression);
        if (!isFinite(result)) {
            throw new Error('Invalid calculation');
        }
        currentInput = result.toString();
        shouldResetDisplay = true;
        updateDisplay();
    } catch (error) {
        showError('Error: Invalid expression');
    }
}
```

## 🔧 Customization

### Changing Colors
Modify the CSS variables in the `<style>` section:
```css
:root {
    --primary-bg: #667eea;
    --secondary-bg: #764ba2;
    --calculator-bg: #2c3e50;
    --display-bg: #34495e;
}
```

### Adding New Functions
1. Add a new button in the HTML structure
2. Create the corresponding JavaScript function
3. Add event listener for the new functionality

### Mobile Optimization
The calculator is already mobile-optimized, but you can adjust:
- Button sizes in CSS
- Font sizes for different screen sizes
- Touch gesture support

## 🐛 Error Handling

The calculator handles various error scenarios:

- **Division by Zero**: Shows "Error: Invalid expression" and resets
- **Invalid Mathematical Operations**: Catches and displays appropriate errors
- **Square Root of Negative Numbers**: Prevents mathematical errors
- **Malformed Expressions**: Gracefully handles syntax errors
- **Overflow/Underflow**: Manages very large or small numbers

![Error Handling](./images/error-handling-web.png)
*Error message display for invalid operations*

## 🌐 Browser Compatibility

| Browser | Version | Support |
|---------|---------|---------|
| Chrome | 60+ | ✅ Full Support |
| Firefox | 55+ | ✅ Full Support |
| Safari | 12+ | ✅ Full Support |
| Edge | 79+ | ✅ Full Support |
| Opera | 47+ | ✅ Full Support |
| Mobile Safari | iOS 12+ | ✅ Full Support |
| Chrome Mobile | Android 8+ | ✅ Full Support |

## 🚀 Deployment Options

### GitHub Pages
1. Push your code to a GitHub repository
2. Go to Settings → Pages
3. Select source branch (main/master)
4. Your calculator will be available at `https://username.github.io/repository-name/calculator.html`

### Local Development Server
```bash
# Python 3
python -m http.server 8000

# Python 2
python -SimpleHTTPServer 8000

# Node.js (if you have it installed)
npx serve .
```

## 🔮 Future Enhancements

- [ ] **Scientific Functions**: sin, cos, tan, log, exponential
- [ ] **Memory Functions**: M+, M-, MR, MC buttons
- [ ] **Calculation History**: View and reuse previous calculations
- [ ] **Themes**: Multiple color schemes and dark/light mode
- [ ] **Unit Converter**: Length, weight, temperature conversions
- [ ] **Graphing**: Simple function plotting capabilities
- [ ] **Voice Input**: Speech recognition for hands-free operation
- [ ] **PWA Support**: Progressive Web App with offline functionality
- [ ] **Export Results**: Save calculations as PDF or text file

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork the repository**
2. **Create a feature branch** (`git checkout -b feature/AmazingFeature`)
3. **Make your changes**:
   - Update HTML structure if needed
   - Modify CSS for styling changes
   - Add JavaScript functionality
   - Update documentation
4. **Test thoroughly** across different browsers and devices
5. **Commit your changes** (`git commit -m 'Add some AmazingFeature'`)
6. **Push to the branch** (`git push origin feature/AmazingFeature`)
7. **Open a Pull Request**

### Contribution Guidelines
- Ensure cross-browser compatibility
- Follow existing code style and formatting
- Add comments for complex functionality
- Test on both desktop and mobile devices
- Update README if you add new features

## 🧪 Testing

### Manual Testing Checklist
- [ ] All number buttons (0-9) work correctly
- [ ] All operator buttons (+, -, *, /) function properly
- [ ] Decimal point operations work as expected
- [ ] Clear and Clear Entry buttons reset appropriately
- [ ] Square root function calculates correctly
- [ ] Sign toggle changes positive/negative values
- [ ] Keyboard shortcuts respond properly
- [ ] Error messages display for invalid operations
- [ ] Calculator works on mobile devices
- [ ] All browsers render the interface correctly

### Automated Testing (Future Enhancement)
```javascript
// Example test structure for future implementation
describe('Calculator Functions', () => {
    test('Basic addition', () => {
        expect(calculate('5+3')).toBe(8);
    });
    
    test('Division by zero', () => {
        expect(calculate('5/0')).toBe('Error: Invalid expression');
    });
});
```

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2025 SATYA PRANEETH MALLIPAM

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.
```

## 👨‍💻 Author

**Your Name**
- GitHub: [@graveinuse](https://github.com/graveinuse)
- Email: smallipa@kent.edu
- Portfolio: 
- LinkedIn: 

## 🙏 Acknowledgments

- **Web Technologies**: HTML5, CSS3, ES6+ JavaScript
- **Design Inspiration**: Modern web design trends and Material Design principles
- **Color Palette**: Inspired by modern gradient designs
- **Icons**: Unicode mathematical symbols for universal compatibility
- **Testing**: Cross-browser compatibility testing tools
- **Community**: Open-source contributors and feedback providers

---

⭐ **Star this repository if you found it helpful!**
