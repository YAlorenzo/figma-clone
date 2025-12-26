# 🎨 figma-clone - Real-Time Collaborative Design Tool


## 📖 About the Project

**Figma-clone** is a powerful, browser-based design tool that enables teams to collaborate in real-time on creative projects. Built with cutting-edge web technologies, it combines the flexibility of a design tool with the power of real-time collaboration.

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

⭐ Star this repo if you find interesting!

