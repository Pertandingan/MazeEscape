# Overview

This project is a hybrid web application that combines a browser-based maze game with a modern full-stack web architecture. The application features two distinct components: a standalone HTML5 canvas maze game ("Maze Escape+") and a React-based web application with 3D graphics capabilities. The maze game is a classic puzzle game where players navigate through increasingly difficult levels, while the React app appears to be set up for more complex interactive experiences with Three.js integration.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture

**Dual Frontend Approach**: The application uses two separate frontend implementations:

1. **Classic Web Game**: Pure HTML5/CSS/JavaScript maze game with canvas-based rendering
   - Vanilla JavaScript class-based architecture (`MazeGame` class)
   - HTML5 Canvas for 2D graphics and game rendering
   - CSS3 for modern UI styling with gradients and animations
   - No framework dependencies for the game logic

2. **Modern React Application**: Built with React 18 and TypeScript
   - Vite as the build tool for fast development and optimized production builds
   - Three.js integration via `@react-three/fiber` and `@react-three/drei` for 3D graphics
   - TailwindCSS for utility-first styling
   - Radix UI components for accessible, headless UI primitives

**State Management**: Uses Zustand for lightweight, flexible state management with middleware support for complex state subscriptions.

**UI Component System**: Comprehensive shadcn/ui component library built on top of Radix UI primitives, providing a consistent design system with dark mode support and accessibility features.

## Backend Architecture

**Express.js Server**: Node.js backend with TypeScript support
- RESTful API architecture with route registration system
- Middleware stack for request logging, JSON parsing, and error handling
- Environment-based configuration for development and production
- Hot reload support via Vite integration in development mode

**Development Setup**: Integrated Vite development server with Express for seamless full-stack development experience.

## Data Storage Solutions

**Database Integration**: 
- PostgreSQL as the primary database with Neon Database serverless hosting
- Drizzle ORM for type-safe database operations and schema management
- Database migrations managed through Drizzle Kit
- Connection pooling and environment-based configuration

**Schema Design**: User-centric data model with authentication-ready user table structure.

**Fallback Storage**: In-memory storage implementation (`MemStorage`) for development and testing scenarios.

## Authentication and Authorization

**Prepared Authentication System**: Basic user schema with username/password fields, ready for implementation of authentication middleware and session management.

**Session Management**: Session infrastructure prepared with `connect-pg-simple` for PostgreSQL-backed sessions.

## External Dependencies

**Core Frameworks:**
- React 18 with TypeScript for modern component-based UI
- Express.js for server-side API handling
- Vite for fast build tooling and development server

**Database & ORM:**
- PostgreSQL for relational data storage
- Neon Database for serverless PostgreSQL hosting
- Drizzle ORM for type-safe database operations
- Drizzle Kit for schema migrations

**3D Graphics & Visualization:**
- Three.js for 3D rendering capabilities
- `@react-three/fiber` for React integration with Three.js
- `@react-three/drei` for common Three.js utilities
- `@react-three/postprocessing` for visual effects

**UI & Styling:**
- TailwindCSS for utility-first styling
- Radix UI for accessible component primitives
- shadcn/ui for pre-built component library
- PostCSS for CSS processing

**State & Data Management:**
- Zustand for client-side state management
- React Query (TanStack Query) for server state management
- React Hook Form for form handling

**Development Tools:**
- TypeScript for type safety across the stack
- ESBuild for fast JavaScript bundling
- Various development utilities for error handling and hot reload

**Audio & Media Support:**
- Built-in audio management system for game sounds
- Support for various audio formats (MP3, OGG, WAV)
- 3D model format support (GLTF, GLB)