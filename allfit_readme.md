# AllFit Website

A comprehensive fitness and women's health platform that connects users with personalized workout plans, nutrition guidance, menstrual cycle tracking, and wellness analytics.

## Overview

AllFit is a modern web application designed to help users achieve their fitness goals through personalized workout routines, meal planning, progress tracking, and community support. Whether you're a beginner starting your fitness journey or an experienced athlete looking to optimize your performance, AllFit provides the tools and guidance you need.

## Features

### Core Functionality
- **Personalized Workout Plans**: Custom exercise routines based on fitness level, goals, and available equipment
- **Nutrition Tracking**: Meal planning and calorie tracking with extensive food database
- **Menstrual Health Monitoring**: AI-powered cycle tracking, period prediction, and reproductive health insights
- **Progress Monitoring**: Visual charts and analytics to track fitness improvements over time
- **Exercise Library**: Comprehensive database of exercises with video demonstrations and instructions
- **Goal Setting**: SMART goal framework with milestone tracking and achievement badges
- **Health Risk Assessment**: PCOS detection, fertility tracking, and personalized health recommendations

### User Experience
- **Responsive Design**: Optimized for desktop, tablet, and mobile devices
- **Interactive Dashboard**: Real-time overview of workouts, nutrition, and progress
- **Social Features**: Community challenges, workout sharing, and motivation network
- **Expert Content**: Articles, tips, and guidance from certified fitness professionals
- **Calendar Integration**: Schedule workouts and meal prep with reminder notifications

## Technology Stack

### Frontend
- **Framework**: React.js with TypeScript
- **Styling**: Tailwind CSS with custom component library
- **State Management**: Redux Toolkit for global state
- **Charts**: Chart.js for progress visualization
- **Authentication**: Firebase Auth integration

### Backend
- **Runtime**: Node.js with Express.js
- **Database**: PostgreSQL with Prisma ORM
- **File Storage**: AWS S3 for media and document storage
- **API**: RESTful API with GraphQL endpoints for complex queries
- **Real-time**: Socket.IO for live features

### DevOps & Tools
- **Deployment**: Docker containers on AWS ECS
- **CI/CD**: GitHub Actions for automated testing and deployment
- **Monitoring**: New Relic for performance monitoring
- **Testing**: Jest and Cypress for unit and integration testing

## Getting Started

### Prerequisites
- Node.js (v18 or higher)
- PostgreSQL (v13 or higher)
- AWS account for cloud services
- Git for version control

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourorg/allfit-website.git
   cd allfit-website
   ```

2. **Install dependencies**
   ```bash
   # Install backend dependencies
   cd backend
   npm install
   
   # Install frontend dependencies
   cd ../frontend
   npm install
   ```

3. **Environment Setup**
   ```bash
   # Copy environment templates
   cp backend/.env.example backend/.env
   cp frontend/.env.example frontend/.env
   ```

4. **Database Setup**
   ```bash
   # Run database migrations
   cd backend
   npx prisma migrate deploy
   npx prisma db seed
   ```

5. **Start Development Servers**
   ```bash
   # Terminal 1: Backend server
   cd backend
   npm run dev
   
   # Terminal 2: Frontend server
   cd frontend
   npm start
   ```

The application will be available at `http://localhost:3000` with the API running on `http://localhost:8000`.

## Project Structure

```
allfit-website/
├── frontend/                 # React application
│   ├── src/
│   │   ├── components/       # Reusable UI components
│   │   ├── pages/           # Route components
│   │   ├── hooks/           # Custom React hooks
│   │   ├── services/        # API service layer
│   │   ├── store/           # Redux store configuration
│   │   └── utils/           # Utility functions
│   ├── public/              # Static assets
│   └── package.json
├── backend/                 # Node.js API server
│   ├── src/
│   │   ├── controllers/     # Route handlers
│   │   ├── models/          # Database models
│   │   ├── middleware/      # Express middleware
│   │   ├── services/        # Business logic
│   │   └── utils/           # Helper functions
│   ├── prisma/              # Database schema and migrations
│   └── package.json
├── docs/                    # Documentation files
├── docker-compose.yml       # Local development environment
└── README.md               # This file
```

## API Documentation

### Authentication Endpoints
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `POST /api/auth/logout` - User logout
- `GET /api/auth/profile` - Get user profile

### Workout Endpoints
- `GET /api/workouts` - List user's workouts
- `POST /api/workouts` - Create new workout
- `GET /api/workouts/:id` - Get specific workout
- `PUT /api/workouts/:id` - Update workout
- `DELETE /api/workouts/:id` - Delete workout

### Nutrition Endpoints
- `GET /api/nutrition/meals` - List meals
- `POST /api/nutrition/meals` - Log meal
- `GET /api/nutrition/foods/search` - Search food database
- `GET /api/nutrition/analytics` - Get nutrition analytics

For complete API documentation, visit `/api/docs` when running the development server.

## Contributing

We welcome contributions to AllFit! Please follow these guidelines:

### Development Workflow
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Make your changes and add tests
4. Ensure all tests pass (`npm test`)
5. Commit with conventional commit messages
6. Push to your fork and submit a pull request

### Code Standards
- Follow ESLint configuration for code formatting
- Write unit tests for new features
- Update documentation for API changes
- Use TypeScript for type safety

### Pull Request Process
- Ensure CI/CD pipeline passes
- Get approval from at least one maintainer
- Squash commits before merging
- Update CHANGELOG.md with your changes

## Testing

### Running Tests
```bash
# Backend tests
cd backend
npm test

# Frontend tests
cd frontend
npm test

# End-to-end tests
npm run test:e2e
```

### Test Coverage
We maintain 80%+ test coverage. Run `npm run test:coverage` to generate coverage reports.

## Deployment

### Production Deployment
1. Build the application: `npm run build`
2. Deploy to AWS ECS using GitHub Actions
3. Run database migrations: `npm run migrate:prod`
4. Verify deployment health checks

### Environment Variables
Key environment variables for production:
- `DATABASE_URL` - PostgreSQL connection string
- `JWT_SECRET` - Authentication token secret
- `AWS_ACCESS_KEY_ID` - AWS credentials
- `STRIPE_SECRET_KEY` - Payment processing

## Security

- All API endpoints require authentication
- Passwords are hashed using bcrypt
- HTTPS enforced in production
- Regular security audits with npm audit
- CORS properly configured for cross-origin requests

## Performance

- Frontend assets are optimized and minified
- Database queries use proper indexing
- CDN integration for static assets
- Lazy loading for improved page speed
- Service workers for offline functionality

## Support

### Getting Help
- Check the [documentation](docs/)
- Search existing [GitHub issues](https://github.com/yourorg/allfit-website/issues)
- Join our [Discord community](https://discord.gg/allfit)
- Email support: support@allfit.com

### Reporting Issues
When reporting bugs, please include:
- Steps to reproduce the issue
- Expected vs actual behavior
- Browser and device information
- Console error messages (if any)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Exercise data provided by [Exercise API](https://exerciseapi.com)
- Nutrition information from [USDA Food Database](https://fdc.nal.usda.gov)
- Icons by [Heroicons](https://heroicons.com)
- Community feedback and contributions from our amazing users

---

**AllFit Team** | [Website](https://allfit.com) | [Twitter](https://twitter.com/allfitapp) | [LinkedIn](https://linkedin.com/company/allfit)