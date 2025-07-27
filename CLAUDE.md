# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a single-page React-based portfolio website called "Nav's Portfolio OS" that simulates a macOS-like desktop environment. The entire application is contained in a single `index.html` file with embedded CSS and React components.

## Architecture

**Single-File Application**: The entire portfolio is built as one HTML file (`index.html`) that includes:
- CSS styles for a macOS-inspired interface with glassmorphism effects
- React components written in JSX using Babel for browser compilation
- Embedded data for experiences, projects, and blog posts

**Key Components**:
- `PortfolioOS`: Root component managing the entire desktop OS interface
- `MainWindowApp`: Main application window with tabbed interface (Professional/Thoughts)
- `PhoneApp`: iPhone simulator showing a Messages app interface
- `Professional`: Search engine-style experience viewer with modal details
- `Thoughts`: Blog post grid with expandable modal posts
- `MacOSModal`: Reusable modal component with fullscreen capability

**Data Structure**: All content (professional experience, projects, extracurriculars, blog posts, conversations) is hardcoded as JavaScript objects within the component definitions.

## Development

**No Build Process**: This is a static HTML file that runs directly in the browser. No compilation, bundling, or build tools are required.

**External Dependencies**:
- React 18 (CDN)
- React DOM 18 (CDN) 
- Babel Standalone (CDN)
- Google Fonts (Inter)
- Spotify embed iframe
- Unsplash background image

**Local Development**: Simply open `index.html` in a web browser or serve it via a local HTTP server.

## Key Features

**Responsive Design**: Mobile devices show a blocker message recommending desktop viewing. The interface is optimized for desktop screens 1025px+ width.

**Interactive Elements**:
- Tabbed navigation between Professional and Thoughts sections
- Modal windows with fullscreen capability (green button)
- Animated typing effects for search interface
- Real-time iPhone Messages simulation with typing animation
- Hover-revealed taskbar at bottom of screen

**Styling Approach**: Uses CSS custom properties for theming with glassmorphism effects, backdrop filters, and macOS-inspired window controls.

## Content Management

To update portfolio content, modify the JavaScript data objects within the `<script>` section:
- `experiencesData`: Professional experience, projects, and extracurriculars
- `blogPosts`: Thought posts displayed in grid format
- `conversations`: iPhone Messages app conversations

## File Assets

The repository includes:
- `index.html`: Main application file
- `logo3_chat.png`: Company logo for Piles
- `wisbusrev.jpg`: Wisconsin Business Review logo

## Technical Notes

**Browser Compatibility**: Requires modern browsers supporting ES6+, CSS backdrop-filter, and React 18.

**Performance**: Single-file architecture means the entire application loads at once. External resources (Spotify embed, images) may affect load times.

**State Management**: Uses React hooks (useState, useEffect) for local component state. No external state management library needed due to application simplicity.