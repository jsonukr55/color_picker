# NgxCustomColorPicker

[![npm version](https://badge.fury.io/js/ngx-custom-color-picker.svg)](https://badge.fury.io/js/ngx-custom-color-picker)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A lightweight, customizable, and dependency-free Angular color picker component built from scratch using Canvas API.

## ✨ Features

- 🎨 **Interactive Color Canvas** - Click and drag to select colors
- 🌈 **Hue Spectrum Bar** - Full 360° hue range selection
- 📝 **Multiple Input Formats** - HEX, RGB, and HSL support
- 📱 **Responsive Design** - Works on mobile and desktop
- 🚫 **Zero Dependencies** - Built using only Angular and Canvas API
- ⚡ **Lightweight** - Minimal bundle size impact
- 🎯 **TypeScript** - Full type safety
- 🔧 **Customizable** - Easy to style and configure

## 📦 Installation

Install the package via npm:

```bash
npm install ngx-custom-color-picker
```

## 🚀 Usage

### 1. Import the Component

Since this is a standalone component, you can import it directly:

```typescript
import { Component } from '@angular/core';
import { NgxColorPickerComponent } from 'ngx-custom-color-picker';

@Component({
  selector: 'app-root',
  standalone: true,
  imports: [NgxColorPickerComponent],
  template: `
    <ngx-color-picker 
      [initialColor]="'#3498db'"
      (colorSelected)="onColorSelected($event)">
    </ngx-color-picker>
  `
})
export class AppComponent {
  onColorSelected(color: string) {
    console.log('Selected color:', color);
  }
}
```

### 2. Module-based Usage (Optional)

If you're using NgModules:

```typescript
import { NgModule } from '@angular/core';
import { NgxColorPickerComponent } from 'ngx-custom-color-picker';

@NgModule({
  imports: [NgxColorPickerComponent],
  // ... other module configuration
})
export class YourModule { }
```

## 📋 API Reference

### Inputs

| Property | Type | Default | Description |
|----------|------|---------|-------------|
| `initialColor` | `string` | `'#ff0000'` | Initial color value in HEX format |

### Outputs

| Event | Type | Description |
|-------|------|-------------|
| `colorSelected` | `EventEmitter<string>` | Emitted when a color is selected. Returns RGB format (e.g., 'rgb(255, 0, 0)') |

### Methods

The component also exports utility methods via `NgxCustomColorPickerService`:

```typescript
import { NgxCustomColorPickerService } from 'ngx-custom-color-picker';

// Convert RGB to HEX
const hex = NgxCustomColorPickerService.rgbToHex(255, 0, 0); // '#ff0000'

// Convert HEX to RGB
const rgb = NgxCustomColorPickerService.hexToRgb('#ff0000'); // { r: 255, g: 0, b: 0 }

// Validate HEX color
const isValid = NgxCustomColorPickerService.isValidHex('#ff0000'); // true

// Generate random color
const randomColor = NgxCustomColorPickerService.getRandomColor(); // '#a1b2c3'
```

## 🎨 Styling

The component comes with default styling, but you can customize it using CSS:

```css
/* Override default styles */
ngx-color-picker .color-picker-container {
  border-radius: 12px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.15);
}

ngx-color-picker .color-preview {
  border-radius: 8px;
}

ngx-color-picker .input-group input {
  border-radius: 6px;
}
```

## 📱 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers with Canvas API support

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Built with Angular and Canvas API
- Inspired by the need for a lightweight, dependency-free color picker
- Thanks to the Angular community for their excellent documentation

## 📞 Support

If you encounter any issues or have questions, please file an issue on [GitHub Issues](https://github.com/yourusername/ngx-custom-color-picker/issues).

---

Made with ❤️ by [Your Name]
