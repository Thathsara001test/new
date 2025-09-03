# Auto X Sri Lanka - Construction Materials & Vehicle Rental Platform

A comprehensive platform connecting construction professionals with vehicle owners and material suppliers across Sri Lanka.

## Features

### For Service Consumers
- Browse and rent construction vehicles (JCBs, excavators, lorries, etc.)
- Source quality construction materials (sand, soil, bricks, gravel, etc.)
- Direct contact with verified suppliers
- Island-wide coverage across all 25 districts

### For Vehicle Owners
- List vehicles for rental
- Set custom rates and availability
- Connect with verified customers
- Earn passive income from vehicle rentals

### For Material Suppliers
- List construction materials
- Expand customer base
- Quality certification support
- Manage orders and deliveries

## Technology Stack

### Frontend
- React 18 with TypeScript
- Tailwind CSS for styling
- Vite for development and building
- Lucide React for icons

### Backend
- Node.js with Express
- MySQL database with Sequelize ORM
- JWT authentication
- File upload support with Multer
- Email notifications with Nodemailer

## Getting Started

### Prerequisites
- Node.js (v16 or higher)
- MySQL database
- npm or yarn package manager

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd autox-platform
   ```

2. **Install frontend dependencies**
   ```bash
   npm install
   ```

3. **Install backend dependencies**
   ```bash
   npm run setup
   ```

4. **Database Setup**
   - Create a MySQL database named `autox_db`
   - Update database credentials in `server/.env`
   - Run database creation script:
   ```bash
   cd server
   node scripts/createDatabase.js
   ```

5. **Seed the database (optional)**
   ```bash
   cd server
   npm run seed
   ```

### Running the Application

1. **Start the backend server**
   ```bash
   npm run server
   ```
   The API will be available at `http://localhost:5000`

2. **Start the frontend development server**
   ```bash
   npm run dev
   ```
   The application will be available at `http://localhost:5173`

## Environment Variables

Create `.env` files in both root and `server` directories with the following variables:

### Database
- `DB_HOST` - MySQL host (default: localhost)
- `DB_PORT` - MySQL port (default: 3306)
- `DB_NAME` - Database name (default: autox_db)
- `DB_USER` - Database username
- `DB_PASSWORD` - Database password

### Authentication
- `JWT_SECRET` - Secret key for JWT tokens
- `JWT_EXPIRE` - Token expiration time (default: 30d)

### Email (Optional)
- `EMAIL_HOST` - SMTP host
- `EMAIL_PORT` - SMTP port
- `EMAIL_USER` - Email username
- `EMAIL_PASS` - Email password

## API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `GET /api/auth/me` - Get current user
- `PUT /api/auth/profile` - Update profile

### Materials
- `GET /api/materials` - Get all materials
- `GET /api/materials/:id` - Get material by ID
- `POST /api/materials` - Create material (Partners only)
- `PUT /api/materials/:id` - Update material
- `DELETE /api/materials/:id` - Delete material

### Vehicles
- `GET /api/vehicles` - Get all vehicles
- `GET /api/vehicles/:id` - Get vehicle by ID
- `POST /api/vehicles` - Create vehicle (Partners only)
- `PUT /api/vehicles/:id` - Update vehicle
- `DELETE /api/vehicles/:id` - Delete vehicle

### Service Requests
- `GET /api/service-requests` - Get user's requests
- `POST /api/service-requests` - Create service request
- `PUT /api/service-requests/:id/status` - Update request status

### Partners
- `POST /api/partners/register` - Partner registration
- `GET /api/partners/me` - Get partner profile
- `PUT /api/partners/me` - Update partner profile

## Project Structure

```
autox-platform/
├── src/                    # Frontend source code
│   ├── components/         # React components
│   ├── data/              # Mock data and constants
│   ├── types/             # TypeScript type definitions
│   └── main.tsx           # Application entry point
├── server/                # Backend source code
│   ├── config/            # Database configuration
│   ├── middleware/        # Express middleware
│   ├── models/            # Sequelize models
│   ├── routes/            # API routes
│   ├── scripts/           # Database scripts
│   └── utils/             # Utility functions
└── public/                # Static assets
```

## Default Users (After Seeding)

- **Admin**: admin@autox.lk / admin123
- **Customer**: john@autox.lk / password123
- **Vehicle Partner**: mike@autox.lk / password123
- **Material Partner**: sarah@autox.lk / password123

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is licensed under the MIT License.

## Support

For support and questions, contact:
- Email: support@autox.lk
- Phone: +94 76 1098385