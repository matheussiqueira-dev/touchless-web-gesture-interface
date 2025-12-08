# Touchless Web Gesture Interface 🖐️

A complete gesture-based interaction system powered by computer vision, running entirely in the browser. This project enables users to create, move, and edit notes, as well as draw on a canvas, all without touching the mouse.

## ✨ Features

- **Virtual Cursor**: Smooth, responsive cursor controlled by hand movements
- **Gesture Recognition**: Stable detection of multiple gestures:
  - 👋 **Open Hand**: Move cursor around
  - 🤏 **Pinch** (Thumb + Index): Click action / Draw on canvas
  - ✊ **Fist**: Drag objects
- **Notes Management**: Create, move, and edit sticky notes using gestures
- **Canvas Drawing**: Draw freely with pinch gestures
- **Modular Architecture**: Clean, reusable React hooks for hand tracking and gesture detection
- **Real-time Processing**: All computer vision runs in the browser using MediaPipe

## 🛠️ Technologies

- **React 19** + **TypeScript**: Modern UI framework with type safety
- **Vite**: Fast build tool and dev server
- **MediaPipe Hands**: Google's hand tracking solution for real-time detection
- **Computer Vision**: 21 hand landmarks for precise gesture recognition

## 📦 Installation

```bash
# Clone the repository
git clone https://github.com/matheussiqueirahub/touchless-web-gesture-interface.git
cd touchless-web-gesture-interface

# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build
```

## 🎮 Usage

1. **Start the application** and click "Start Tracking"
2. **Allow camera access** when prompted
3. **Position your hand** in front of the camera
4. **Use gestures** to interact:

### Notes Mode
- **Quick Pinch**: Create a new note at cursor position
- **Fist over note**: Grab and drag the note
- **Double-click note**: Edit content (using mouse/keyboard)

### Drawing Mode
- **Pinch and hold**: Draw on canvas
- **Release pinch**: Stop drawing
- **Click "Clear Canvas"**: Reset drawing

### Controls
- **Switch Mode**: Toggle between Notes and Drawing modes
- **Show/Hide Help**: Display gesture instructions
- **Stop Tracking**: Pause hand tracking

## 🏗️ Architecture

### Modular Hook System

#### `useHandTracking`
- Manages MediaPipe Hands initialization
- Handles camera access and video streaming
- Processes video frames and extracts 21 hand landmarks
- Returns hand position data in real-time

#### `useGestureEngine`
- Analyzes hand landmarks to detect gestures
- Implements smooth cursor tracking with interpolation
- Provides gesture stabilization to prevent jitter
- Detects: pinch, fist, and open hand gestures

### Components

- **VirtualCursor**: Visual feedback for hand position with color-coded gesture states
- **NotesBoard**: Manages sticky notes with gesture-based interactions
- **DrawingCanvas**: Canvas for free-form drawing with gestures
- **Note**: Individual note component with edit/delete functionality

## 🧪 Testing

The application can be tested by:
1. Running `npm run dev` and accessing `http://localhost:5173`
2. Testing different gestures in both Notes and Drawing modes
3. Verifying smooth cursor tracking and gesture stability

## 🎯 Use Cases

Perfect for portfolios showcasing:
- **Computer Vision**: Browser-based hand tracking
- **Accessibility**: Touch-free interfaces for inclusive design
- **Natural Interaction**: Contactless gesture control
- **Frontend Innovation**: Advanced React patterns and real-time processing

## 🔧 Development

```bash
# Run linter
npm run lint

# Build for production
npm run build

# Preview production build
npm run preview
```

## 📝 License

This project is open source and available for portfolio and educational purposes.

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

## 👤 Author

**Matheus Siqueira**
- GitHub: [@matheussiqueirahub](https://github.com/matheussiqueirahub)

---

Built with ❤️ using React, TypeScript, and MediaPipe
