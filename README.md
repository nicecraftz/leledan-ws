# leledan-ws

A professional portfolio website for **leledan06**, a professional Minecraft builder specializing in organic creations, advanced terraforming, and epic structures. Built with Nuxt 3 and modern web technologies.

## 🎯 Overview

This is a responsive portfolio website showcasing Minecraft building services, featuring an elegant design with smooth animations, interactive galleries, and comprehensive service information.

## ✨ Features

### 🏠 Home Page
- **Animated Hero Section**: Dynamic background with crossfade transitions and breathing animations
- **About Section**: Personal introduction highlighting expertise in organic builds, terraforming, and architectural structures
- **Skills Showcase**: Interactive display of technical competencies including:
  - Organic sculptures (animals, humans, creatures)
  - Botany and flora design
  - Terrain sculpting and terraforming
  - Architecture (various styles)
  - Lighting expertise
  - Video editing
  - Skin creation
- **Customer Marquee**: Scrolling showcase of clients and collaborators (YouTubers and servers)

### 🖼️ Portfolio Page
- **Interactive Gallery**: Grid display of 45+ Minecraft build examples
- **Image Popup Viewer**: Click-to-expand functionality with full-screen modal
- **Responsive Grid**: Adaptive layout (1-3 columns based on screen size)
- **Hover Effects**: Visual feedback with border color transitions and eye icon overlay

### 💼 Services Page
- **Pricing Plans**: Six service categories with detailed pricing:
  - **Costruzione** (Sculptures): €50 - €300+
  - **Strutture Avanzate** (Advanced Structures): €200 - €500
  - **Costruzioni Base** (Basic Builds): €50 - €150
  - **Terraforming**: €150 - €400
  - **Skin Creation**: €20 - €50
  - **Progetti Custom** (Custom Projects): Quote-based
- **Feature Lists**: Each service includes delivery timelines and included features

### ⭐ Reviews Page
- **Customer Testimonials**: Detailed reviews from satisfied clients
- **Alternating Layout**: Reviews displayed with alternating left/right image placement
- **Client Information**: Shows customer avatars, roles (YouTuber/Server), and subscriber counts
- **5-Star Ratings**: Visual star rating system

### 📄 Terms of Service (TOS)
- **Comprehensive Terms**: Detailed service agreement covering:
  - Commitment and project selection
  - Deadlines and delivery process
  - Content restrictions
  - Revision policies
  - Communication guidelines
  - Usage rights
  - Payment terms

### 🎨 Design Features
- **Modern UI**: Built with Nuxt UI and Tailwind CSS
- **Responsive Design**: Mobile-first approach with breakpoints for all screen sizes
- **Smooth Animations**: Transitions, hover effects, and interactive elements
- **Custom Color Scheme**: Primary, secondary, and accent colors with theme support
- **Image Optimization**: WebP format for optimal performance using Nuxt Image

### 🔗 Navigation & Footer
- **Sticky Navigation Bar**: Always accessible with smooth scroll behavior
- **Social Media Links**: Integration with Discord, Twitter, Instagram, YouTube, Gmail, Telegram, and TikTok
- **Footer**: Copyright information and social media icons with glow effects

## 🛠️ Tech Stack

- **Framework**: [Nuxt 4.2.2](https://nuxt.com/)
- **UI Library**: [Nuxt UI 4.2.1](https://ui.nuxt.com/)
- **Styling**: [Tailwind CSS 4.1.18](https://tailwindcss.com/)
- **Image Optimization**: [Nuxt Image 2.0.0](https://image.nuxt.com/)
- **Language**: TypeScript 5.6.3
- **Runtime**: Vue 3.5.25

## 📁 Project Structure

```
leledan-ws/
├── app/
│   ├── assets/
│   │   └── css/
│   │       └── main.css
│   ├── components/
│   │   ├── CustomerCard.vue
│   │   ├── CustomerMarquee.vue
│   │   ├── HomeHero.vue
│   │   ├── NavBar.vue
│   │   ├── PageFooter.vue
│   │   ├── Review.vue
│   │   ├── ServiceCard.vue
│   │   ├── SkillIcon.vue
│   │   ├── SkillsBar.vue
│   │   └── WhoAmI.vue
│   ├── layouts/
│   │   └── default.vue
│   ├── pages/
│   │   ├── index.vue
│   │   ├── portfolio.vue
│   │   ├── reviews.vue
│   │   ├── services.vue
│   │   └── tos.vue
│   └── app.vue
├── public/
│   ├── background/        # Hero background images
│   ├── customers/        # Client avatars
│   ├── images/           # Logo and profile images
│   ├── portfolio/        # 45+ build showcase images
│   └── resources/        # SVG assets
├── nuxt.config.ts
└── package.json
```

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ or Bun
- Package manager (npm, pnpm, yarn, or bun)

### Installation

```bash
# Install dependencies
bun install
# or
npm install
# or
pnpm install
# or
yarn install
```

### Development

Start the development server:

```bash
bun run dev
# or
npm run dev
# or
pnpm dev
# or
yarn dev
```

The application will be available at `http://localhost:3000`

### Build

Build for production:

```bash
bun run build
# or
npm run build
# or
pnpm build
# or
yarn build
```

### Preview

Preview the production build locally:

```bash
bun run preview
# or
npm run preview
# or
pnpm preview
# or
yarn preview
```

### Generate Static Site

Generate a static site:

```bash
bun run generate
# or
npm run generate
# or
pnpm generate
# or
yarn generate
# or
npx nuxi generate
```

## 📝 Key Components

- **NavBar**: Responsive navigation with icon-based menu items
- **HomeHero**: Animated hero section with background transitions
- **WhoAmI**: Personal introduction and profile section
- **SkillsBar**: Technical skills display with icons
- **CustomerMarquee**: Infinite scrolling customer showcase
- **ServiceCard**: Reusable pricing card component
- **Review**: Customer testimonial component with alternating layouts
- **PageFooter**: Footer with social media links and copyright

## 🎨 Customization

The project uses a custom color scheme defined in Tailwind CSS. Key colors include:
- `primary`: Main brand color
- `secondary`: Accent color
- `background`: Page background
- `text`: Text color
- `foreground`: Foreground elements

## 📱 Responsive Breakpoints

- Mobile: Default (< 640px)
- Tablet: `sm:` (≥ 640px)
- Desktop: `md:` (≥ 768px)
- Large Desktop: `lg:` (≥ 1024px)

## 🔍 SEO

- Meta tags configured for title and description
- Semantic HTML structure
- Optimized images with WebP format
- Robots.txt included

## 📄 License

Private project - All rights reserved.

---

**Built with ❤️ for the Minecraft building community**
