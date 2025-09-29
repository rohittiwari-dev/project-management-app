# 🚀 Project Management System - Frontend Client

A modern React frontend application for the project management system, built with TypeScript, Vite, Tailwind CSS, and cutting-edge UI libraries. Provides an intuitive and responsive interface for workspace collaboration and project management.

## ✨ Features

### 🎨 Modern UI/UX

- **Responsive Design**: Mobile-first approach with Tailwind CSS
- **Component Library**: Built with Radix UI primitives for accessibility
- **Interactive Components**:
  - Data tables with sorting, filtering, and pagination
  - Dialog modals for forms and confirmations
  - Toast notifications for user feedback
  - Loading skeletons for better UX
  - Emoji picker for reactions
  - Date picker for task scheduling

### 🏢 Workspace Interface

- **Multi-workspace Dashboard**: Switch between multiple workspaces
- **Workspace Analytics**: Visual charts and metrics
- **Member Management**: Invite and manage team members
- **Role-based UI**: Show/hide features based on user permissions

### 📊 Project Management

- **Project Dashboard**: Overview of all projects in workspace
- **Project Creation**: Intuitive project setup forms
- **Project Analytics**: Track project progress with visual indicators

### ✅ Task Management

- **Kanban Board**: Drag-and-drop task management
- **Task Status Tracking**: Visual status indicators
- **Priority Management**: Color-coded priority levels
- **Task Filtering**: Advanced filtering and search capabilities

### 🔐 Authentication

- **Login/Register Forms**: Clean authentication interface
- **Google OAuth**: One-click Google sign-in
- **Session Management**: Automatic session handling
- **Protected Routes**: Route-based authentication

## 🛠️ Tech Stack

### Core Framework

- **Framework**: React 18 with TypeScript
- **Build Tool**: Vite 6
- **Routing**: React Router DOM v7

### Styling & UI

- **CSS Framework**: Tailwind CSS 3.4
- **Component Library**: Radix UI primitives
- **Icons**: Lucide React
- **Utilities**:
  - class-variance-authority for component variants
  - tailwind-merge for className optimization
  - tailwindcss-animate for animations
  - clsx for conditional classes

### State Management

- **Global State**: Zustand 4
- **Server State**: TanStack Query (React Query) 5
- **URL State**: nuqs for URL state management

### Forms & Validation

- **Forms**: React Hook Form 7
- **Validation**: Zod schema validation
- **Form Resolvers**: @hookform/resolvers for Zod integration

### Data & Utilities

- **HTTP Client**: Axios
- **Date Handling**: date-fns
- **Immutable Updates**: Immer
- **Data Tables**: TanStack Table 8
- **Date Picker**: React Day Picker
- **Command Menu**: cmdk

### UI Enhancements

- **Emoji Support**: emoji-mart with React integration
- **Scroll Areas**: Radix UI scroll areas
- **Tooltips**: Radix UI tooltips
- **Popovers**: Radix UI popovers

## 📁 Project Structure

```
client/
├── public/
│   ├── vite.svg
│   └── images/
│       └── workspace.jpg
├── src/
│   ├── components/          # React components
│   │   ├── ui/             # Reusable UI components
│   │   ├── workspace/      # Workspace-specific components
│   │   ├── auth/           # Authentication components
│   │   ├── header.tsx      # Main header component
│   │   ├── asidebar/       # Sidebar components
│   │   ├── confirm-dialog/ # Confirmation dialogs
│   │   ├── emoji-picker/   # Emoji picker component
│   │   ├── logo/           # Logo components
│   │   ├── resuable/       # Reusable components
│   │   └── skeleton-loaders/ # Loading skeletons
│   ├── hooks/              # Custom React hooks
│   │   ├── use-confirm-dialog.tsx
│   │   ├── use-create-project-dialog.tsx
│   │   ├── use-create-workspace-dialog.tsx
│   │   ├── use-mobile.tsx
│   │   ├── use-permissions.ts
│   │   ├── use-task-table-filter.ts
│   │   └── use-toast.ts
│   ├── context/            # React contexts
│   │   ├── auth-provider.tsx
│   │   └── query-provider.tsx
│   ├── hoc/                # Higher-order components
│   │   └── with-permission.tsx
│   ├── lib/                # Utility libraries
│   ├── layout/             # Layout components
│   ├── page/               # Page components
│   ├── routes/             # Route definitions
│   ├── types/              # TypeScript type definitions
│   ├── constant/           # Application constants
│   ├── assets/             # Static assets
│   ├── App.tsx             # Main App component
│   ├── main.tsx            # Application entry point
│   ├── index.css           # Global styles
│   └── vite-env.d.ts       # Vite environment types
├── components.json         # shadcn/ui configuration
├── tailwind.config.js      # Tailwind CSS configuration
├── postcss.config.js       # PostCSS configuration
├── vite.config.ts          # Vite configuration
├── tsconfig.json           # TypeScript configuration
├── tsconfig.app.json       # App-specific TypeScript config
├── tsconfig.node.json      # Node-specific TypeScript config
├── eslint.config.js        # ESLint configuration
└── package.json
```

## 🚀 Getting Started

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn package manager
- Backend API server running

### Environment Variables

Create a `.env` file in the client directory:

```env
# API Configuration
VITE_API_BASE_URL=http://localhost:5000/api
VITE_BACKEND_URL=http://localhost:5000

# Google OAuth (if needed for client-side)
VITE_GOOGLE_CLIENT_ID=your-google-client-id

# Environment
VITE_NODE_ENV=development
```

### Installation & Setup

1. **Install dependencies**

```bash
npm install
```

2. **Start development server**

```bash
npm run dev
```

3. **Build for production**

```bash
npm run build
```

4. **Preview production build**

```bash
npm run preview
```

5. **Lint code**

```bash
npm run lint
```

The application will be available at http://localhost:5173

## 🎨 Component Architecture

### UI Components (`/components/ui/`)

Base components built with Radix UI primitives:

- Button, Input, Label, Select
- Dialog, Popover, Tooltip
- Table, Tabs, Separator
- Avatar, Checkbox, ScrollArea

### Feature Components

- **Workspace Components**: Workspace creation, management, analytics
- **Project Components**: Project dashboard, creation forms
- **Task Components**: Task boards, forms, filters
- **Auth Components**: Login, register, OAuth buttons

### Layout Components

- **Header**: Navigation and user menu
- **Sidebar**: Workspace and project navigation
- **Layout**: Main application layout structure

## 🔧 Custom Hooks

### UI Hooks

- `useToast`: Toast notification management
- `useMobile`: Responsive design utilities
- `useConfirmDialog`: Confirmation dialog state

### Business Logic Hooks

- `usePermissions`: Role-based permission checking
- `useTaskTableFilter`: Task filtering and search
- `useCreateWorkspaceDialog`: Workspace creation flow
- `useCreateProjectDialog`: Project creation flow

## 🌐 State Management

### Global State (Zustand)

- User authentication state
- Current workspace context
- UI state (sidebar, modals)

### Server State (TanStack Query)

- API data caching and synchronization
- Optimistic updates
- Background refetching
- Error and loading states

### Local State

- Form state with React Hook Form
- Component-specific state with useState
- URL state with nuqs

## 🎯 Route Structure

```
/                           # Landing page
/auth/login                 # Login page
/auth/register              # Registration page
/auth/callback              # OAuth callback
/workspace/:id              # Workspace dashboard
/workspace/:id/projects     # Projects list
/workspace/:id/projects/:projectId  # Project details
/workspace/:id/settings     # Workspace settings
/workspace/:id/members      # Member management
```

## 🎨 Styling System

### Tailwind CSS Configuration

- Custom color palette
- Responsive breakpoints
- Animation utilities
- Component variants

### Design System

- Consistent spacing scale
- Typography hierarchy
- Color tokens
- Shadow system

### Component Variants

```typescript
// Example button variants
const buttonVariants = cva(
  "inline-flex items-center justify-center rounded-md text-sm font-medium",
  {
    variants: {
      variant: {
        default: "bg-primary text-primary-foreground hover:bg-primary/90",
        destructive:
          "bg-destructive text-destructive-foreground hover:bg-destructive/90",
        outline:
          "border border-input hover:bg-accent hover:text-accent-foreground",
        secondary:
          "bg-secondary text-secondary-foreground hover:bg-secondary/80",
        ghost: "hover:bg-accent hover:text-accent-foreground",
        link: "text-primary underline-offset-4 hover:underline",
      },
      size: {
        default: "h-10 px-4 py-2",
        sm: "h-9 rounded-md px-3",
        lg: "h-11 rounded-md px-8",
        icon: "h-10 w-10",
      },
    },
    defaultVariants: {
      variant: "default",
      size: "default",
    },
  }
);
```

## 📱 Responsive Design

### Breakpoints

- `sm`: 640px and up
- `md`: 768px and up
- `lg`: 1024px and up
- `xl`: 1280px and up
- `2xl`: 1536px and up

### Mobile-First Approach

- Components adapt to screen size
- Touch-friendly interactions
- Optimized navigation for mobile

## 🔒 Authentication Flow

### Login Process

1. User enters credentials or uses Google OAuth
2. Frontend sends request to backend API
3. Backend validates and creates session
4. Frontend receives user data and updates state
5. Protected routes become accessible

### Route Protection

```typescript
// HOC for protected routes
const withPermission = (WrappedComponent, requiredPermissions) => {
  return (props) => {
    const { hasPermission } = usePermissions();

    if (!hasPermission(requiredPermissions)) {
      return <UnauthorizedComponent />;
    }

    return <WrappedComponent {...props} />;
  };
};
```

## 🧪 Testing

```bash
# Run tests (if implemented)
npm test

# Run tests in watch mode
npm run test:watch

# Run test coverage
npm run test:coverage
```

## 🚀 Deployment

### Build Process

```bash
npm run build
```

### Deployment Options

- **Vercel**: Automatic deployment with Git integration
- **Netlify**: Static site deployment
- **AWS S3 + CloudFront**: Scalable static hosting
- **Docker**: Containerized deployment

### Environment Configuration

Set production environment variables:

- API endpoints
- OAuth credentials
- Feature flags

## 📦 Build Configuration

### Vite Configuration

- TypeScript support
- React plugin
- Path aliases
- Environment variables
- Build optimizations

### TypeScript Configuration

- Strict type checking
- Path mapping
- JSX support
- Module resolution

## 🤝 Contributing

### Development Guidelines

1. Use TypeScript for all components
2. Follow React best practices
3. Use Tailwind CSS for styling
4. Implement proper error boundaries
5. Write accessible components
6. Follow the existing project structure

### Code Style

- Use ESLint configuration
- Follow naming conventions
- Write self-documenting code
- Use proper TypeScript types

## 📞 Support

For frontend-specific issues, please check:

1. Browser console for errors
2. Network tab for API issues
3. Component props and state
4. Routing configuration

---

Built with ❤️ using React, TypeScript, and modern web technologies
