# Inventory Management System

A comprehensive full-stack inventory management application built with modern web technologies. This system provides real-time analytics, product management, user administration, and expense tracking capabilities.

## 🌟 Features

### Dashboard & Analytics
- **Real-time Metrics**: Live dashboard with key performance indicators
- **Sales Analytics**: Interactive charts showing sales trends and performance
- **Purchase Tracking**: Monitor purchasing patterns and costs
- **Expense Management**: Categorized expense tracking with visual breakdowns
- **Popular Products**: Track best-selling items and inventory levels

### Product Management
- **Product Catalog**: Complete product listing with search functionality
- **Inventory Tracking**: Real-time stock quantity monitoring
- **Product Creation**: Easy-to-use forms for adding new products
- **Rating System**: Customer rating integration for products
- **Price Management**: Dynamic pricing with historical tracking

### User Management
- **User Directory**: Complete user management system
- **Role-based Access**: Secure user authentication and authorization
- **Profile Management**: User profile and settings management

### System Features
- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile
- **Dark/Light Mode**: Toggle between themes for better user experience
- **Search & Filtering**: Advanced search capabilities across all modules
- **Data Export**: Export data for reporting and analysis

## 🏗️ Architecture

### Frontend (Client)
- **Framework**: Next.js 14 with React 18
- **Styling**: Tailwind CSS with custom theme system
- **State Management**: Redux Toolkit with RTK Query for API calls
- **UI Components**: Material-UI Data Grid, Lucide React icons
- **Charts**: Recharts for data visualization
- **Type Safety**: Full TypeScript implementation

### Backend (Server)
- **Runtime**: Node.js with Express.js
- **Database**: PostgreSQL with Prisma ORM
- **API**: RESTful API with proper error handling
- **Security**: Helmet.js, CORS, and input validation
- **Logging**: Morgan for request logging

## 🚀 Getting Started

### Prerequisites
- Node.js (v18 or higher)
- PostgreSQL database
- npm or yarn package manager

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd inventory-management
   ```

2. **Install dependencies**
   
   For the server:
   ```bash
   cd server
   npm install
   ```
   
   For the client:
   ```bash
   cd client
   npm install
   ```

3. **Database Setup**
   
   Create a `.env` file in the server directory:
   ```env
   DATABASE_URL="postgresql://username:password@localhost:5432/inventory_db"
   PORT=8000
   ```

4. **Initialize the database**
   ```bash
   cd server
   npx prisma migrate dev
   npm run seed
   ```

5. **Start the development servers**
   
   Start the backend server:
   ```bash
   cd server
   npm run dev
   ```
   
   Start the frontend application:
   ```bash
   cd client
   npm run dev
   ```

6. **Access the application**
   - Frontend: http://localhost:3000
   - Backend API: http://localhost:8000

## 📱 Usage Guide

### For Business Users

**Dashboard Overview**
- View key metrics at a glance including sales, purchases, and expenses
- Monitor popular products and inventory levels
- Track performance trends with interactive charts

**Managing Products**
- Navigate to "Products" to view your complete inventory
- Use the search bar to quickly find specific items
- Click "Create Product" to add new items to your catalog
- Monitor stock levels and update pricing as needed

**Tracking Expenses**
- Visit the "Expenses" section for detailed expense analysis
- Filter expenses by category (Office, Professional, Salaries)
- Use date filters to analyze spending patterns over time
- View visual breakdowns with interactive pie charts

**User Management**
- Access the "Users" section to manage team members
- View user details and contact information
- Monitor user activity and permissions

### For Developers

**Project Structure**
```
inventory-management/
├── client/                 # Next.js frontend application
│   ├── src/
│   │   ├── app/           # App router pages and components
│   │   ├── state/         # Redux store and API definitions
│   │   └── ...
├── server/                # Express.js backend API
│   ├── src/
│   │   ├── controllers/   # Route handlers
│   │   ├── routes/        # API route definitions
│   │   └── index.ts       # Server entry point
│   └── prisma/           # Database schema and migrations
```

**API Endpoints**
- `GET /dashboard` - Dashboard metrics and analytics
- `GET /products` - Product listing with optional search
- `POST /products` - Create new product
- `GET /users` - User management data
- `GET /expenses` - Expense data by category

**Database Schema**
The system uses PostgreSQL with the following main entities:
- **Products**: Product catalog with pricing and inventory
- **Sales**: Transaction records and sales data
- **Purchases**: Purchase orders and supplier data
- **Users**: User accounts and profiles
- **Expenses**: Categorized business expenses

**Development Commands**
```bash
# Database operations
npx prisma migrate dev     # Run migrations
npx prisma generate        # Generate Prisma client
npm run seed              # Seed database with sample data

# Development
npm run dev               # Start development server
npm run build             # Build for production
npm start                 # Start production server
```

## 🔧 Configuration

### Environment Variables

**Server (.env)**
```env
DATABASE_URL=postgresql://username:password@localhost:5432/inventory_db
PORT=8000
NODE_ENV=development
```

**Client (.env.local)**
```env
NEXT_PUBLIC_API_BASE_URL=http://localhost:8000
```

### Customization

**Themes**: Modify `client/tailwind.config.ts` to customize colors and styling
**API Base URL**: Update the API base URL in the client environment variables
**Database**: Configure PostgreSQL connection in the server environment variables

## 🚀 Deployment

### Production Deployment

1. **Build the applications**
   ```bash
   # Build server
   cd server && npm run build
   
   # Build client
   cd client && npm run build
   ```

2. **Set production environment variables**
3. **Deploy to your preferred hosting platform**

### AWS EC2 Deployment
Detailed EC2 deployment instructions are available in `server/aws-ec2-instructions.md`

## 🛠️ Technology Stack

### Frontend Technologies
- **Next.js 14**: React framework with app router
- **TypeScript**: Type-safe development
- **Tailwind CSS**: Utility-first CSS framework
- **Redux Toolkit**: State management with RTK Query
- **Material-UI**: Data grid components
- **Recharts**: Chart and visualization library

### Backend Technologies
- **Node.js**: JavaScript runtime
- **Express.js**: Web application framework
- **Prisma**: Modern database toolkit and ORM
- **PostgreSQL**: Relational database
- **TypeScript**: Type-safe server development

### Development Tools
- **ESLint**: Code linting and formatting
- **Prettier**: Code formatting
- **Prisma Studio**: Database management interface

## 📊 Data Models

### Core Entities
- **Products**: Inventory items with pricing, ratings, and stock levels
- **Sales**: Transaction records with quantities and amounts
- **Purchases**: Purchase orders and supplier transactions
- **Users**: System users and authentication data
- **Expenses**: Business expenses categorized by type

## 🔒 Security Features

- **Input Validation**: Server-side validation for all API endpoints
- **CORS Protection**: Configured cross-origin resource sharing
- **Helmet.js**: Security headers and protection
- **Type Safety**: Full TypeScript implementation prevents runtime errors

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🆘 Support

For technical support or questions:
- Check the documentation above
- Review the code comments and type definitions
- Open an issue in the repository for bugs or feature requests

## 🔄 Version History

- **v1.0.0**: Initial release with core inventory management features
- Dashboard analytics and reporting
- Product and user management
- Expense tracking and categorization