# 🧼 Sistem Manajemen Kebersihan Kantor

A modern, comprehensive cleaning service management system built with Next.js 15, TypeScript, and Prisma. This system helps offices manage cleaning schedules, track employee performance, and monitor facility cleanliness through an intuitive web interface.

## ✨ Features

### 🏢 Core Management
- **Employee Management**: Manage cleaning staff with roles, schedules, and contracts
- **Room/Area Management**: Organize office spaces by type, floor, and cleaning requirements
- **Schedule Management**: Create and assign cleaning tasks with time tracking
- **Real-time Monitoring**: Live dashboard with statistics and progress tracking

### 📊 Reporting & Analytics
- **Daily Reports**: Comprehensive cleaning completion reports with photos
- **Performance Metrics**: Track employee performance and cleaning quality
- **Visual Analytics**: Charts and graphs for management insights
- **Export Functionality**: Generate reports in various formats

### 🔐 Authentication & Security
- **Role-based Access**: Admin and employee roles with appropriate permissions
- **Secure Login**: Password-based authentication with session management
- **Data Protection**: Secure handling of sensitive information

### 📱 Modern UI/UX
- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile
- **Dark Mode**: Built-in theme switching for user comfort
- **Real-time Updates**: Live notifications and status updates
- **Interactive Elements**: Smooth animations and micro-interactions

## 🛠️ Technology Stack

### Frontend
- **⚡ Next.js 15** - React framework with App Router
- **📘 TypeScript 5** - Type-safe development
- **🎨 Tailwind CSS 4** - Modern utility-first CSS
- **🧩 shadcn/ui** - High-quality UI components
- **🎯 Lucide React** - Beautiful icons
- **🌈 Framer Motion** - Smooth animations

### Backend & Database
- **🗄️ Prisma** - Modern ORM with TypeScript
- **🔐 bcryptjs** - Password hashing
- **📡 Socket.IO** - Real-time communication
- **🌐 RESTful APIs** - Clean API architecture

### Development Tools
- **🔍 ESLint** - Code quality and consistency
- **🎣 React Hook Form** - Form management
- **✅ Zod** - Schema validation
- **🐻 Zustand** - State management

## 🚀 Quick Start

### Prerequisites
- Node.js 18+ 
- npm or yarn
- Git

### Installation

```bash
# Clone the repository
git clone <your-repo-url>
cd manajemen-kebersihan

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env

# Generate Prisma client
npx prisma generate

# Set up database
npx prisma db push

# Seed initial data (optional)
npm run db:seed

# Start development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to view the application.

### Default Login Credentials
- **Admin**: `admin` / `admin123`
- **Employee**: `budi` / `pegawai123`

## 📁 Project Structure

```
src/
├── app/                    # Next.js App Router
│   ├── api/               # API routes
│   ├── dashboard/         # Dashboard pages
│   └── globals.css        # Global styles
├── components/
│   └── ui/                # shadcn/ui components
├── hooks/                 # Custom React hooks
├── lib/                   # Utilities and configurations
└── prisma/                # Database schema and migrations
```

## 🌐 Deployment

### Vercel (Recommended)

1. **Prepare for Deployment**
   ```bash
   # Install Vercel CLI
   npm i -g vercel
   
   # Login to Vercel
   npx vercel login
   ```

2. **Set Environment Variables**
   In Vercel Dashboard → Settings → Environment Variables:
   ```bash
   DATABASE_URL=your_postgresql_connection_string
   NEXTAUTH_URL=https://your-app.vercel.app
   NEXTAUTH_SECRET=your_random_secret_key
   NODE_ENV=production
   ```

3. **Deploy**
   ```bash
   npx vercel --prod
   ```

📖 **Detailed deployment guide**: See [DEPLOYMENT.md](./DEPLOYMENT.md)

### Other Platforms

The application is compatible with:
- **Netlify** (with serverless functions)
- **AWS Amplify**
- **DigitalOcean App Platform**
- **Railway**
- **Render**

## 🗄️ Database Setup

### Development (SQLite)
```bash
# Push schema to SQLite
npx prisma db push

# View database
npx prisma studio
```

### Production (PostgreSQL)
1. Set up a PostgreSQL database
2. Update `DATABASE_URL` environment variable
3. Run migrations: `npx prisma db push`

## 📊 Features Overview

### Dashboard Admin
- **Overview**: Real-time statistics and metrics
- **Employee Management**: Add, edit, and manage staff
- **Schedule Management**: Create and assign cleaning tasks
- **Room Management**: Organize facility spaces
- **Report Management**: Review and verify cleaning reports
- **Office Management**: Manage multiple office locations

### Dashboard Pegawai
- **Personal Schedule**: View assigned cleaning tasks
- **Task Completion**: Mark tasks as complete with photos
- **Report History**: Track past cleaning activities
- **Performance Metrics**: View personal performance stats

### Real-time Features
- **Live Notifications**: Instant updates for task assignments
- **Status Tracking**: Real-time progress monitoring
- **Chat Support**: Internal communication system

## 🔧 Configuration

### Environment Variables
```bash
# Database
DATABASE_URL="file:./dev.db"                    # Development
# DATABASE_URL="postgresql://..."               # Production

# Authentication
NEXTAUTH_URL="http://localhost:3000"            # Development
# NEXTAUTH_URL="https://your-app.vercel.app"    # Production
NEXTAUTH_SECRET="your-secret-key-here"

# Application
NODE_ENV="development"
```

## 🧪 Testing & Quality

```bash
# Run linting
npm run lint

# Fix linting issues
npm run lint:fix

# Type checking
npm run type-check

# Build for production
npm run build
```

## 📝 API Documentation

### Authentication
- `POST /api/auth/login` - User authentication

### Employees
- `GET /api/pegawai` - List all employees
- `POST /api/pegawai` - Create new employee
- `PUT /api/pegawai/[id]` - Update employee
- `DELETE /api/pegawai/[id]` - Delete employee

### Schedules
- `GET /api/jadwal` - List all schedules
- `POST /api/jadwal` - Create new schedule
- `PUT /api/jadwal/[id]` - Update schedule
- `DELETE /api/jadwal/[id]` - Delete schedule

### Reports
- `GET /api/laporan` - List all reports
- `POST /api/laporan` - Create new report
- `GET /api/laporan/export` - Export reports

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit changes: `git commit -m 'Add amazing feature'`
4. Push to branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

For support and questions:
- Create an issue in the repository
- Check the [DEPLOYMENT.md](./DEPLOYMENT.md) for deployment help
- Review the API documentation above

---

Built with ❤️ for modern office management. Clean spaces, happy teams! 🧼✨
