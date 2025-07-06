# TaskFlow - Task Management Web Application

## Overview

TaskFlow is a full-stack task management web application built with modern technologies. It provides users with the ability to create, manage, and collaborate on tasks with real-time updates. The application features social authentication, task sharing capabilities, and a responsive design that works across desktop and mobile devices.

## System Architecture

### Frontend Architecture
- **Framework**: React with TypeScript
- **Build Tool**: Vite for fast development and optimized builds
- **Routing**: Wouter for lightweight client-side routing
- **State Management**: TanStack Query (React Query) for server state management
- **UI Components**: Radix UI primitives with custom shadcn/ui components
- **Styling**: Tailwind CSS with CSS variables for theming
- **Real-time Communication**: WebSocket client for live updates

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **Database**: PostgreSQL with Drizzle ORM
- **Authentication**: Replit Auth with OAuth 2.0 (social logins)
- **Session Management**: Express sessions with PostgreSQL storage
- **Real-time Communication**: WebSocket server for task updates
- **API Design**: RESTful API with proper error handling and validation

### Database Architecture
- **ORM**: Drizzle with type-safe schema definitions
- **Database**: PostgreSQL (configured for Neon serverless)
- **Schema**: Shared between client and server for type safety
- **Migrations**: Managed through Drizzle Kit

## Key Components

### Authentication System
- **Provider**: Replit Auth integration
- **Flow**: OAuth 2.0 with social login support
- **Session Storage**: PostgreSQL-based session store
- **Security**: HTTP-only cookies with CSRF protection

### Task Management
- **CRUD Operations**: Full create, read, update, delete functionality
- **Task Properties**: Title, description, status, priority, due dates
- **Task Sharing**: Email-based sharing with other users
- **Real-time Updates**: WebSocket-based live synchronization

### User Interface
- **Design System**: Modern, accessible components using Radix UI
- **Responsiveness**: Mobile-first design with Tailwind CSS
- **Theme Support**: CSS custom properties for consistent theming
- **Error Handling**: Comprehensive error boundaries and user feedback

### Real-time Features
- **WebSocket Connection**: Per-user connection management
- **Live Updates**: Automatic task synchronization across clients
- **Offline Support**: Basic offline capabilities with error handling

## Data Flow

1. **User Authentication**: Users sign in through social providers via Replit Auth
2. **Session Management**: Authenticated sessions stored in PostgreSQL
3. **Task Operations**: API requests validated and processed through Express middleware
4. **Database Updates**: Changes persisted via Drizzle ORM with type safety
5. **Real-time Broadcast**: Task updates broadcast to affected users via WebSocket
6. **Client Updates**: Frontend receives updates and synchronizes UI state

## External Dependencies

### Database
- **Provider**: Neon PostgreSQL (serverless)
- **Connection**: Pooled connections via @neondatabase/serverless
- **Configuration**: Environment-based DATABASE_URL

### Authentication
- **Provider**: Replit Auth service
- **Configuration**: OIDC discovery with environment variables
- **Session Storage**: PostgreSQL table for session persistence

### UI Libraries
- **Component Library**: Radix UI for accessible primitives
- **Icons**: Lucide React for consistent iconography
- **Styling**: Tailwind CSS with shadcn/ui configuration
- **Forms**: React Hook Form with Zod validation

### Development Tools
- **Build**: Vite with React plugin and TypeScript support
- **Database Management**: Drizzle Kit for schema management
- **Type Safety**: Shared TypeScript schemas between client/server

## Deployment Strategy

### Build Process
- **Frontend**: Vite builds optimized static assets
- **Backend**: esbuild creates Node.js bundle for production
- **Output**: Separate dist directories for client and server

### Environment Configuration
- **Database**: PostgreSQL connection via DATABASE_URL
- **Authentication**: Replit Auth configuration
- **Sessions**: Secure session secret for production

### Production Considerations
- **Static Assets**: Frontend built to dist/public for static serving
- **Server Bundle**: Backend compiled to single ESM file
- **Environment Variables**: Required for database and auth configuration

## Changelog

Changelog:
- July 05, 2025. Initial setup

## User Preferences

Preferred communication style: Simple, everyday language.