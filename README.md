# 🎨 Tigma - Real-Time Collaborative Design Tool

> A modern, real-time collaborative design tool inspired by Figma. Create, collaborate, and design together with live cursors, comments, and instant synchronization.

[![Next.js](https://img.shields.io/badge/Next.js-14.1.0-black?style=for-the-badge&logo=next.js)](https://nextjs.org/)
[![React](https://img.shields.io/badge/React-18.2-blue?style=for-the-badge&logo=react)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue?style=for-the-badge&logo=typescript)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-3.4-38bdf8?style=for-the-badge&logo=tailwind-css)](https://tailwindcss.com/)
[![Liveblocks](https://img.shields.io/badge/Liveblocks-Real--time-ff6b6b?style=for-the-badge)](https://liveblocks.io/)
[![Fabric.js](https://img.shields.io/badge/Fabric.js-5.3-purple?style=for-the-badge)](http://fabricjs.com/)

---

## 📸 Demo & Screenshots

### 🚀 Live Demo
**[🚧 Add your deployment link here - Vercel/Netlify]**

### 🖼️ App Screenshot
![App Screenshot](path/to/screenshot.png)

> **Note:** Replace `path/to/screenshot.png` with your actual screenshot path or add a GIF demonstration showing the real-time collaboration features.

---

## 📖 About the Project

**Tigma** is a powerful, browser-based design tool that enables teams to collaborate in real-time on creative projects. Built with cutting-edge web technologies, it combines the flexibility of a design tool with the power of real-time collaboration.

### 🎯 Problem It Solves

- **Real-time Collaboration**: Multiple designers can work simultaneously without conflicts
- **No Installation Required**: Fully browser-based, works on any device
- **Instant Synchronization**: See changes from team members in real-time
- **Interactive Communication**: Built-in chat, comments, and reactions for seamless team interaction

### ✨ Key Features

✅ **Real-time Collaborative Canvas** - Multiple users editing simultaneously  
✅ **Drawing Tools** - Freeform drawing and shape tools (rectangle, circle, triangle, line)  
✅ **Text Editing** - Rich text formatting with multiple fonts, sizes, and weights  
✅ **Image Upload** - Drag and drop images directly onto the canvas  
✅ **Live Cursors** - See where team members are working in real-time  
✅ **Cursor Chat** - Communicate with team members via cursor-based chat (`/` key)  
✅ **Comments System** - Threaded comments for feedback and discussions  
✅ **Reactions** - Express quick feedback with emoji reactions (`E` key)  
✅ **Layer Management** - Organize and manage design layers efficiently  
✅ **Shape Properties** - Customize colors, dimensions, alignment, and more  
✅ **Undo/Redo** - Full history support with keyboard shortcuts  
✅ **Export to PDF** - Export your designs as PDF files  
✅ **Keyboard Shortcuts** - Power user features with intuitive shortcuts  
✅ **Context Menu** - Right-click for quick actions  

---

## 🛠️ Technology Stack

### Core Framework
- **[Next.js 14.1.0](https://nextjs.org/)** - React framework with App Router
- **[React 18](https://react.dev/)** - UI library
- **[TypeScript 5](https://www.typescriptlang.org/)** - Type safety

### Real-time Collaboration
- **[Liveblocks](https://liveblocks.io/)** - Real-time collaboration infrastructure
  - `@liveblocks/client` - Core client library
  - `@liveblocks/react` - React hooks and providers
  - `@liveblocks/react-comments` - Comments system

### Canvas & Graphics
- **[Fabric.js 5.3](http://fabricjs.com/)** - Powerful canvas library for interactive graphics

### Styling & UI
- **[Tailwind CSS 3.4](https://tailwindcss.com/)** - Utility-first CSS framework
- **[Radix UI](https://www.radix-ui.com/)** - Accessible component primitives
  - `@radix-ui/react-context-menu` - Context menus
  - `@radix-ui/react-dropdown-menu` - Dropdown menus
  - `@radix-ui/react-select` - Select components
  - `@radix-ui/react-label` - Form labels
  - `@radix-ui/react-tooltip` - Tooltips
- **[Lucide React](https://lucide.dev/)** - Beautiful icon library
- **[Tailwind Animate](https://tailwindcss-animate.com/)** - Animation utilities

### Utilities
- **[jsPDF](https://github.com/parallax/jsPDF)** - PDF generation
- **[UUID](https://github.com/uuidjs/uuid)** - Unique ID generation
- **[clsx](https://github.com/lukeed/clsx)** - Conditional class names
- **[class-variance-authority](https://cva.style/)** - Component variant management

### Development Tools
- **ESLint** - Code linting
- **Prettier** - Code formatting
- **TypeScript** - Static type checking

---

## 📁 Project Structure

```
figma-clone/
├── app/                      # Next.js App Router
│   ├── App.tsx              # Main application component
│   ├── Room.tsx             # Liveblocks room provider wrapper
│   ├── page.tsx             # Home page
│   ├── layout.tsx           # Root layout
│   └── globals.css          # Global styles
│
├── components/              # React components
│   ├── comments/           # Comment system components
│   │   ├── Comments.tsx
│   │   ├── CommentsOverlay.tsx
│   │   ├── NewThread.tsx
│   │   ├── NewThreadCursor.tsx
│   │   ├── PinnedComposer.tsx
│   │   └── PinnedThread.tsx
│   │
│   ├── cursor/             # Live cursor components
│   │   ├── Cursor.tsx
│   │   ├── CursorChat.tsx
│   │   └── LiveCursors.tsx
│   │
│   ├── reaction/           # Reaction components
│   │   ├── FlyingReaction.tsx
│   │   ├── ReactionButton.tsx
│   │   └── index.module.css
│   │
│   ├── settings/           # Property panels
│   │   ├── Color.tsx
│   │   ├── Dimensions.tsx
│   │   ├── Export.tsx
│   │   └── Text.tsx
│   │
│   ├── users/              # User-related components
│   │   ├── ActiveUsers.tsx
│   │   ├── Avatar.tsx
│   │   ├── Avatar.module.css
│   │   └── index.module.css
│   │
│   ├── ui/                 # Reusable UI components (Radix UI)
│   │   ├── button.tsx
│   │   ├── context-menu.tsx
│   │   ├── dropdown-menu.tsx
│   │   ├── input.tsx
│   │   ├── label.tsx
│   │   └── select.tsx
│   │
│   ├── LeftSidebar.tsx     # Layers panel
│   ├── RightSidebar.tsx    # Properties panel
│   ├── Live.tsx            # Main canvas component
│   ├── Loader.tsx          # Loading state
│   ├── Navbar.tsx          # Top navigation bar
│   └── ShapesMenu.tsx      # Shapes toolbar
│
├── lib/                    # Utility functions
│   ├── canvas.ts           # Fabric.js canvas operations
│   ├── key-events.ts       # Keyboard event handlers
│   ├── shapes.ts           # Shape creation/modification
│   ├── useMaxZIndex.ts     # Z-index management
│   └── utils.ts            # General utilities
│
├── hooks/                  # Custom React hooks
│   └── useInterval.ts      # Interval hook
│
├── types/                  # TypeScript type definitions
│   ├── type.ts             # Main type definitions
│   └── declaration.d.ts    # Type declarations
│
├── constants/              # App constants
│   └── index.ts            # Shape configs, colors, shortcuts
│
├── public/                 # Static assets
│   └── assets/             # Icons and images
│
├── liveblocks.config.ts    # Liveblocks configuration
├── tailwind.config.ts      # Tailwind CSS configuration
├── next.config.mjs         # Next.js configuration
├── tsconfig.json           # TypeScript configuration
└── package.json            # Dependencies and scripts
```

---

## 🚀 Getting Started

### Prerequisites

- **Node.js** 18+ and npm/yarn/pnpm
- **Liveblocks API Key** - Get yours at [liveblocks.io](https://liveblocks.io)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/figma-clone.git
   cd figma-clone
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or
   yarn install
   # or
   pnpm install
   ```

3. **Set up environment variables**
   
   Create a `.env.local` file in the root directory:
   ```env
   NEXT_PUBLIC_LIVEBLOCKS_PUBLIC_KEY=your_liveblocks_public_key_here
   ```

4. **Run the development server**
   ```bash
   npm run dev
   # or
   yarn dev
   # or
   pnpm dev
   ```

5. **Open your browser**
   
   Navigate to [http://localhost:3000](http://localhost:3000)

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `/` | Open cursor chat |
| `E` | Open reaction selector |
| `Esc` | Close chat/reactions |
| `Ctrl/Cmd + Z` | Undo |
| `Ctrl/Cmd + Y` | Redo |
| `Delete` | Delete selected object |
| `Right-click` | Open context menu |

---

## 🎨 Features in Detail

### Real-time Collaboration
- Multiple users can work on the same canvas simultaneously
- Live cursor tracking shows where each team member is working
- Instant synchronization of all changes across all clients

### Drawing & Shapes
- **Freeform Drawing**: Draw freely on the canvas
- **Predefined Shapes**: Rectangle, Circle, Triangle, Line
- **Customizable Properties**: Colors, dimensions, stroke width

### Text Editing
- Multiple font families (Helvetica, Times New Roman, Comic Sans MS, Brush Script MT)
- Font sizes from 10px to 36px
- Font weights (Normal, Semibold, Bold)
- Text alignment options

### Comments & Communication
- **Threaded Comments**: Create comment threads on specific canvas locations
- **Cursor Chat**: Quick chat messages attached to your cursor
- **Reactions**: Quick emoji reactions for fast feedback

### Layer Management
- View all objects as layers in the left sidebar
- Click layers to select corresponding objects on canvas
- Visual hierarchy representation

### Export & Sharing
- Export canvas to PDF format
- All designs are automatically saved via Liveblocks storage

---

## 🧩 Core Technologies Explained

### Liveblocks
Liveblocks provides the real-time synchronization layer. It handles:
- **Presence**: Live cursor positions and user states
- **Storage**: Persistent canvas objects (LiveMap)
- **Events**: Broadcasting reactions and other events
- **Comments**: Threaded commenting system

### Fabric.js
Fabric.js powers the canvas functionality:
- Object creation and manipulation
- Drawing paths and shapes
- Image handling
- Selection and transformation
- Event handling

### Next.js App Router
Modern React framework features:
- Server Components and Client Components
- Optimized bundle splitting
- Built-in routing
- Image optimization

---

## 🔧 Available Scripts

```bash
# Development
npm run dev          # Start development server

# Production
npm run build        # Build for production
npm run start        # Start production server

# Code Quality
npm run lint         # Run ESLint
```

---

## 🌐 Deployment

### Vercel (Recommended)

1. Push your code to GitHub
2. Import your repository on [Vercel](https://vercel.com)
3. Add your environment variables:
   - `NEXT_PUBLIC_LIVEBLOCKS_PUBLIC_KEY`
4. Deploy!

### Other Platforms

This Next.js app can be deployed on:
- **Netlify**
- **AWS Amplify**
- **Railway**
- **Any Node.js hosting platform**

---

## 📝 Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `NEXT_PUBLIC_LIVEBLOCKS_PUBLIC_KEY` | Your Liveblocks public API key | ✅ Yes |

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 🙏 Acknowledgments

- [Figma](https://www.figma.com) - Inspiration for the design
- [Liveblocks](https://liveblocks.io) - Real-time collaboration infrastructure
- [Fabric.js](http://fabricjs.com/) - Canvas manipulation library
- [Radix UI](https://www.radix-ui.com/) - Accessible component primitives

---

## 📞 Contact & Support

- **Issues**: [GitHub Issues](https://github.com/yourusername/figma-clone/issues)
- **Discussions**: [GitHub Discussions](https://github.com/yourusername/figma-clone/discussions)

---

<div align="center">

**Made with ❤️ and TypeScript**

⭐ Star this repo if you find it helpful!

</div>
