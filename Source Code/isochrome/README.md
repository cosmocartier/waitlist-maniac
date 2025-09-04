# ISOChrome - Creative Agency Portfolio

A modern, high-end portfolio website for creative agencies, built with Next.js 15 and advanced animation technologies. ISOChrome showcases creative work with sophisticated animations, smooth transitions, and a premium user experience.

## 🚀 Features

### Core Technologies
- **Next.js 15** - React framework with App Router
- **React 18** - Latest React features and hooks
- **GSAP (GreenSock)** - Professional-grade animations
- **Lenis** - Smooth scrolling library
- **View Transitions API** - Native page transitions
- **SplitType** - Text splitting for animations

### Key Features
- **Advanced Animation System** - Custom GSAP animations with custom easing curves
- **Smooth Page Transitions** - Native View Transitions API implementation
- **Text Animations** - Line-by-line text splitting and animation
- **Parallax Effects** - Smooth parallax scrolling
- **Preloader** - Custom loading screen with progress bar
- **Responsive Design** - Mobile-first approach
- **Dark Theme** - Sophisticated dark color palette
- **Custom Typography** - Druk and Akkurat Mono fonts

### Site Structure
- **Home** - Hero section with animated content
- **About** - Company/agency information
- **Work** - Portfolio showcase
- **Project** - Individual project details
- **Contact** - Contact information and form

## 📋 Prerequisites

Before running this application, ensure you have the following installed:

- **Node.js** (v18.0.0 or higher)
- **npm** (v9.0.0 or higher) or **pnpm** (v8.0.0 or higher) or **yarn** (v1.22.0 or higher)

## 🛠️ Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd isochrome
   ```

2. **Install dependencies**
   ```bash
   # Using npm
   npm install
   
   # Using pnpm (recommended)
   pnpm install
   
   # Using yarn
   yarn install
   ```

3. **Set up environment variables** (if needed)
   ```bash
   # Create .env.local file
   touch .env.local
   ```

## 🚀 Development

### Running the Development Server

```bash
# Using npm
npm run dev

# Using pnpm
pnpm dev

# Using yarn
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

### Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run start` - Start production server
- `npm run lint` - Run ESLint

## 🏗️ Project Structure

```
isochrome/
├── public/                 # Static assets
│   ├── about/             # About page images
│   ├── client-logos/      # Client logo assets
│   ├── contact/           # Contact page images
│   ├── fonts/             # Custom fonts
│   ├── home/              # Home page images
│   ├── project/           # Project page images
│   └── projects/          # Project showcase images
├── src/
│   └── app/               # Next.js App Router
│       ├── about/         # About page
│       ├── components/    # Reusable components
│       │   ├── AnimatedCopy/
│       │   ├── AnimatedH1/
│       │   ├── Footer/
│       │   ├── Nav/
│       │   └── ParallaxImage/
│       ├── contact/       # Contact page
│       ├── project/       # Project page
│       ├── work/          # Work/Portfolio page
│       ├── globals.css    # Global styles
│       ├── layout.js      # Root layout
│       └── page.js        # Home page
├── package.json           # Dependencies and scripts
├── next.config.mjs        # Next.js configuration
└── jsconfig.json          # JavaScript configuration
```

## 🎨 Customization

### Styling
The application uses CSS custom properties for theming. Main variables are defined in `src/app/globals.css`:

```css
:root {
  --bg: #1a1a1a;        /* Background color */
  --copy: #bac4b8;      /* Text color */
}
```

### Fonts
Custom fonts are loaded from the `public/fonts/` directory:
- **Druk** family (Bold, Heavy, Medium, Super)
- **Akkurat Mono** (Regular)

### Animations
GSAP animations are configured with custom easing curves. The main custom ease is defined in the home page:

```javascript
CustomEase.create(
  "hop-main",
  "M0,0 C0.354,0 0.464,0.133 0.498,0.502 0.532,0.872 0.651,1 1,1"
);
```

## 🚀 Production Deployment

### Building for Production

```bash
# Build the application
npm run build

# Start production server
npm run start
```

### Deployment Options

#### Vercel (Recommended)
1. Connect your repository to Vercel
2. Vercel will automatically detect Next.js and deploy
3. No additional configuration needed

#### Netlify
1. Build command: `npm run build`
2. Publish directory: `.next`
3. Add environment variables if needed

#### Traditional Server
1. Build the application: `npm run build`
2. Copy the `.next` folder to your server
3. Install dependencies: `npm install --production`
4. Start the server: `npm run start`

### Environment Variables
Create a `.env.local` file for local development or set environment variables in your deployment platform:

```env
# Add any required environment variables here
NEXT_PUBLIC_SITE_URL=https://yourdomain.com
```

## 📦 Dependencies

### Core Dependencies
- `next: 15.1.7` - React framework
- `react: ^18.0.0` - React library
- `react-dom: ^18.0.0` - React DOM

### Animation Dependencies
- `gsap: ^3.12.7` - Professional animation library
- `@gsap/react: ^2.1.2` - GSAP React integration
- `lenis: ^1.1.21` - Smooth scrolling
- `@studio-freight/react-lenis: ^0.0.47` - React Lenis integration
- `split-type: ^0.3.4` - Text splitting for animations

### UI/UX Dependencies
- `next-view-transitions: ^0.3.4` - View Transitions API support

## 🔧 Configuration

### Next.js Configuration
The application uses a minimal Next.js configuration in `next.config.mjs`. Add any additional configuration as needed:

```javascript
/** @type {import('next').NextConfig} */
const nextConfig = {
  // Add your custom configuration here
  images: {
    domains: ['your-domain.com'],
  },
  // Enable experimental features if needed
  experimental: {
    // Add experimental features
  }
};

export default nextConfig;
```

### JavaScript Configuration
Path aliases are configured in `jsconfig.json`:

```json
{
  "compilerOptions": {
    "paths": {
      "@/*": ["./src/*"]
    }
  }
}
```

## 🐛 Troubleshooting

### Common Issues

1. **Port already in use**
   ```bash
   # Kill process on port 3000
   lsof -ti:3000 | xargs kill -9
   ```

2. **GSAP animations not working**
   - Ensure GSAP is properly registered
   - Check browser console for errors
   - Verify ScrollTrigger is registered if using scroll animations

3. **Fonts not loading**
   - Check if font files exist in `public/fonts/`
   - Verify font-face declarations in CSS

4. **Build errors**
   ```bash
   # Clear Next.js cache
   rm -rf .next
   npm run build
   ```

## 📱 Browser Support

- Chrome 111+
- Firefox 111+
- Safari 16.4+
- Edge 111+

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🆘 Support

For support and questions:
- Create an issue in the repository
- Contact the development team
- Check the documentation

---

**Built with ❤️ using Next.js and GSAP**
