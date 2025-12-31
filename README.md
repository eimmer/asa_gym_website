# ASA Gym Manager Website

A Flutter web application for managing gym operations, built with Flutter for the web platform.

## 📋 Overview

ASA Gym Manager is a Progressive Web App (PWA) designed to help manage gym-related operations. The application provides a modern, responsive web interface built with Flutter's web framework.

## 🚀 Technology Stack

- **Framework**: Flutter Web
- **Language**: Dart
- **Platform**: Web (PWA)
- **Theme Color**: #0175C2

## ✨ Features

- Progressive Web App (PWA) support - installable on devices
- Responsive design for desktop and mobile devices
- Modern Material Design UI components
- Cross-platform web compatibility

## 📦 Installation & Setup

### Prerequisites

- [Flutter SDK](https://flutter.dev/docs/get-started/install) (latest stable version)
- Dart SDK (included with Flutter)
- A modern web browser

### Getting Started

1. **Clone the repository** (if applicable):
   ```bash
   git clone <repository-url>
   cd gym_manager_website
   ```

2. **Install dependencies**:
   ```bash
   flutter pub get
   ```

3. **Run the development server**:
   ```bash
   flutter run -d chrome
   ```

   Or use any other available web device:
   ```bash
   flutter devices  # List available devices
   flutter run -d <device-id>
   ```

## 🏗️ Building for Production

### Build the Web Application

```bash
flutter build web --base-href /asa_gym_website/
```

This command will:
- Compile the Dart code to JavaScript
- Generate optimized assets
- Create a production-ready build in the `build/web` directory

### Build Options

- **Base href**: The app is configured to be served from `/asa_gym_website/` path
- **Release mode**: Optimized build with minified code (default for `flutter build web`)
- **Web renderer**: Uses CanvasKit by default for better performance

## 🚢 Deployment

### Deployment Steps

1. Build the application:
   ```bash
   flutter build web --base-href /asa_gym_website/
   ```

2. Deploy the contents of the `build/web` directory to your web server

3. Ensure your web server is configured to:
   - Serve files from the correct base path (`/asa_gym_website/`)
   - Handle client-side routing correctly
   - Serve with appropriate MIME types for Flutter web assets

### Server Configuration

Make sure your web server:
- Serves `index.html` for all routes (SPA routing)
- Sets proper caching headers for static assets
- Supports HTTPS (recommended for PWA features)

## 📁 Project Structure

```
gym_manager_website/
├── assets/              # Application assets
│   └── images/          # Image files (including ASA logo)
├── icons/               # PWA icons (192x192, 512x512)
├── canvaskit/           # CanvasKit rendering engine files
├── index.html           # Main HTML entry point
├── manifest.json        # PWA manifest configuration
├── version.json         # Application version information
└── [build artifacts]    # Compiled JavaScript and assets
```

## 🔧 Configuration

### PWA Manifest

The application is configured as a Progressive Web App. Settings can be modified in `manifest.json`:
- App name: `asa_gyms`
- Theme color: `#0175C2`
- Display mode: `standalone`
- Icons: Multiple sizes for various devices

### Base Path

The application is configured to run under the `/asa_gym_website/` path. To change this:
1. Update the `<base href>` in `index.html`
2. Rebuild with the new base-href parameter:
   ```bash
   flutter build web --base-href /your-new-path/
   ```

## 🧪 Development

### Running in Development Mode

```bash
flutter run -d chrome --web-port 8080
```

### Hot Reload

Flutter supports hot reload during development. Press `r` in the terminal to reload, or `R` for a full restart.

### Debugging

- Use Chrome DevTools for debugging
- Flutter DevTools provides additional debugging capabilities
- Run `flutter pub run build_runner watch` if using code generation

## 📱 PWA Features

This application is configured as a Progressive Web App, which means:
- It can be installed on devices (desktop and mobile)
- It works offline (depending on service worker configuration)
- It has app-like behavior and appearance
- It uses modern web APIs for enhanced functionality

## 🔒 Security Considerations

- Always serve the application over HTTPS in production
- Keep dependencies updated regularly
- Review and configure Content Security Policy as needed
- Validate and sanitize user inputs

## 📝 Version Information

- **Version**: 1.0.0
- **Build Number**: 1
- **Package Name**: asa_gyms

## 🤝 Contributing

1. Create a feature branch
2. Make your changes
3. Test thoroughly
4. Submit a pull request

## 📄 License

[Specify your license here]

## 👥 Support

For issues, questions, or contributions, please [create an issue](link-to-issues) or contact the development team.