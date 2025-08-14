# SecureChat - End-to-End Encrypted Messaging

## Overview

SecureChat is a secure messaging application built with modern web technologies, featuring end-to-end encryption for private conversations. The application uses RSA encryption for key exchange and AES-256 for message content encryption, ensuring that only the intended recipients can read messages. Built as a full-stack application with Express.js backend and React frontend, it integrates with Replit's authentication system and provides real-time messaging through WebSockets.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **React 18** with TypeScript for the user interface
- **Vite** as the build tool and development server
- **Tailwind CSS** with shadcn/ui components for styling and UI components
- **TanStack Query** for server state management and API communication
- **Wouter** for lightweight client-side routing
- **Web Crypto API** for client-side encryption operations

### Backend Architecture
- **Express.js** server with TypeScript
- **Drizzle ORM** with PostgreSQL for database operations
- **WebSocket** server for real-time messaging
- **Passport.js** with OpenID Connect for Replit authentication
- **Session-based authentication** with PostgreSQL session storage

### Database Design
The application uses PostgreSQL with the following key tables:
- **users** - User profiles with RSA public keys
- **conversations** - Chat containers
- **conversation_participants** - Many-to-many relationship between users and conversations
- **messages** - Encrypted message storage with sender metadata
- **user_keys** - User encryption key management
- **sessions** - Session storage for authentication

### Security Architecture
- **End-to-End Encryption**: Messages are encrypted client-side using AES-256
- **RSA Key Exchange**: 2048-bit RSA keys for secure AES key distribution
- **Client-Side Encryption**: All sensitive operations happen in the browser
- **Secure Key Storage**: Public keys stored on server, private keys remain client-side
- **Session Security**: HTTP-only cookies with secure session management

### Real-Time Communication
- **WebSocket Server**: Custom WebSocket implementation for instant messaging
- **Connection Management**: Automatic reconnection with exponential backoff
- **Typing Indicators**: Real-time typing status updates
- **Message Delivery**: Instant message delivery with encryption status indicators

### Authentication System
- **Replit OAuth Integration**: Uses Replit's OpenID Connect provider
- **Session Management**: PostgreSQL-backed session storage with connect-pg-simple
- **User Profile Sync**: Automatic user creation and profile updates from Replit

## External Dependencies

### Core Infrastructure
- **Neon Database**: PostgreSQL serverless database hosting
- **Replit Authentication**: OAuth 2.0 / OpenID Connect identity provider
- **WebSocket Protocol**: Real-time bidirectional communication

### Key Libraries and Services
- **@neondatabase/serverless**: PostgreSQL database driver optimized for serverless
- **drizzle-orm**: Type-safe ORM for database operations
- **@radix-ui/react-***: Accessible UI component primitives
- **@tanstack/react-query**: Server state management and caching
- **passport** + **openid-client**: Authentication middleware and OIDC client
- **ws**: WebSocket server implementation
- **nanoid**: Secure random ID generation

### Development and Build Tools
- **Vite**: Frontend build tool and development server
- **TypeScript**: Static type checking across frontend and backend
- **Tailwind CSS**: Utility-first CSS framework
- **ESBuild**: Fast JavaScript/TypeScript bundler for production builds