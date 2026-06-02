# BK Mine - README

> **Reservation and queue management platform for handcrafted food sellers**

[![Build Status](https://img.shields.io/badge/build-passing-brightgreen)]()
[![License](https://img.shields.io/badge/license-MIT-blue)]()
[![React Native](https://img.shields.io/badge/react%20native-0.74-61dafb?logo=react)]()
[![TypeScript](https://img.shields.io/badge/typescript-5.3-blue?logo=typescript)]()

## Overview

BK Mine is a mobile-first application that helps handcrafted food sellers manage their daily limited inventory through a smart reservation and queue management system. It prevents line cutting, overcrowding, and reservation confusion.

### Key Problems It Solves
- ❌ Prevent line cutting and overcrowding
- ❌ Manage limited daily inventory efficiently
- ❌ Reduce confusion with clear reservation tracking
- ❌ Provide fair queue management system
- ❌ Enable real-time inventory updates

## Features

### 🛍️ Customer Features
- **Browse Sessions** - View active food selling sessions with details
- **Reserve Items** - Quick reservation ("Mine" feature) with instant inventory deduction
- **Track Queue** - Monitor your position and estimated wait time
- **View History** - See past reservations and claims
- **Notifications** - Real-time updates on reservations and queue status
- **Profile Management** - Manage personal information and preferences

### 👨‍🍳 Seller (Host) Features
- **Session Management** - Create, edit, and close selling sessions
- **Inventory Control** - Set products, quantities, and per-customer limits
- **Reservation Control** - Approve or reject reservation requests
- **Live Queue Monitor** - See real-time queue with customer information
- **Sales Reports** - Track total sold, revenue, and inventory status

### 👨‍💼 Admin Features
- **User Management** - Manage customers and sellers
- **Session Moderation** - Review and moderate all sessions
- **System Analytics** - View platform-wide metrics and insights
- **Content Management** - Manage system-wide settings

## Tech Stack

- **Frontend Framework**: React Native + Expo Router
- **Language**: TypeScript
- **State Management**: Zustand
- **Backend**: Supabase (PostgreSQL)
- **Authentication**: Supabase Auth
- **Styling**: NativeWind (Tailwind for React Native)
- **Real-time**: Supabase Realtime
- **Deployment**: EAS (Expo Application Services)

## Quick Start

### Prerequisites
- Node.js 18+
- npm or yarn
- Expo account
- Supabase account

### Installation

```bash
# Clone repository
git clone https://github.com/jezreelpilapil-lab/bk-mine.git
cd bk-mine

# Install dependencies
npm install

# Setup environment variables
cp .env.example .env
# Edit .env with your Supabase credentials

# Start development server
npm start

# Run on iOS
npm run ios

# Run on Android
npm run android

# Run on Web
npm run web
```

## Documentation

- 📖 [Setup Guide](./SETUP.md) - Detailed setup instructions
- 🚀 [Deployment Guide](./DEPLOYMENT.md) - How to build and deploy
- 🏗️ [Architecture Guide](./ARCHITECTURE.md) - Project structure and design patterns
- 📚 [Database Schema](./scripts/database-schema.sql) - SQL schema and RLS policies

## Project Structure

```
bk-mine/
├── src/
│   ├── app/                    # Expo Router pages
│   ├── components/             # Reusable UI components
│   ├── features/               # Feature modules (auth, sessions, etc.)
│   ├── lib/                    # Utilities (supabase, theme, validators)
│   ├── hooks/                  # Custom React hooks
│   ├── types/                  # TypeScript definitions
│   └── utils/                  # Helper functions
├── scripts/                    # Setup and utility scripts
├── app.json                    # Expo configuration
├── package.json                # Dependencies
└── README.md                   # This file
```

## User Roles

### Customer
- Browse and reserve items
- Track queue position
- Manage reservations
- View notifications

### Host (Seller)
- Create and manage sessions
- Control inventory
- Approve/reject reservations
- Monitor live queue
- View reports

### Admin
- Manage all users
- Moderate sessions
- View analytics
- System configuration

## Database Models

### Core Tables
- **users** - User profiles and authentication
- **sessions** - Food selling sessions with location and time
- **products** - Items available in sessions
- **reservations** - Customer reservations with status tracking
- **queue_entries** - Queue positions and status
- **notifications** - System notifications

### Security
- Row Level Security (RLS) policies on all tables
- User data isolation
- Role-based access control

## API Integration

### Authentication
```typescript
const { signIn, signUp, signOut } = useAuth();
await signIn(email, password);
```

### Sessions
```typescript
const { sessions, isLoading } = useSessions();
```

### Reservations
```typescript
const { createReservation, myReservations } = useReservations();
```

### Real-time Updates
```typescript
// Automatic real-time subscriptions for reservations and queue
const { reservations } = useReservations(); // Auto-subscribed
```

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Code Standards

- TypeScript for type safety
- Zustand for predictable state
- Functional components with hooks
- Custom hooks for logic reuse
- Error handling with try-catch
- Validation with Zod schemas

## Performance

- 📱 Optimized for mobile-first experience
- ⚡ Lazy loading and pagination
- 💾 Smart caching strategies
- 🔄 Real-time updates via subscriptions
- 📦 Optimized bundle size

## Security

- 🔐 Encrypted authentication tokens
- 🛡️ Row Level Security policies
- ✅ Input validation with Zod
- 🚫 CORS protection
- 🔑 Environment variable management

## Roadmap

- [ ] Session management screens
- [ ] Reservation system
- [ ] Queue monitoring
- [ ] Advanced search and filters
- [ ] User ratings and reviews
- [ ] Direct messaging
- [ ] Social sharing
- [ ] Analytics dashboard
- [ ] Push notifications

## Troubleshooting

### Build Issues
```bash
# Clear cache and reinstall
rm -rf node_modules package-lock.json
npm install

# Clear Expo cache
rm -rf .expo
```

### Database Connection
- Verify Supabase URL in `.env`
- Check anon key is correct
- Ensure Supabase project is active

### Authentication Issues
- Check email exists
- Verify password requirements
- Ensure auth schema is up to date

## Support

- 📧 Email: support@bk-mine.app
- 🐛 [Report Issues](https://github.com/jezreelpilapil-lab/bk-mine/issues)
- 💬 [Discussions](https://github.com/jezreelpilapil-lab/bk-mine/discussions)

## License

MIT © 2024 BK Mine

## Acknowledgments

- Built with [Expo](https://expo.dev)
- Powered by [Supabase](https://supabase.com)
- Styled with [NativeWind](https://www.nativewind.dev)
- State management with [Zustand](https://github.com/pmndrs/zustand)

---

Made with ❤️ for food sellers and customers
