# Laravel API

A RESTful API built with Laravel 12, Vue 3, and SQLite.

## Requirements

- PHP 8.2+
- Composer
- Node.js & npm
- SQLite

## Local Setup Instructions

### 1. Clone the Repository

\`\`\`bash
git clone git@github.com:LucianoNicacio/laravel_api.git
cd laravel_api
\`\`\`

### 2. Install Dependencies

\`\`\`bash
# Install PHP dependencies
composer install

# Install JavaScript dependencies
npm install
\`\`\`

### 3. Environment Configuration

\`\`\`bash
# Copy environment file
cp .env.example .env

# Generate application key
php artisan key:generate
\`\`\`

### 4. Database Setup

This project uses SQLite for development.

\`\`\`bash
# Create SQLite database file
touch database/database.sqlite

# Run migrations
php artisan migrate

# (Optional) Seed the database
php artisan db:seed
\`\`\`

### 5. Storage Setup

\`\`\`bash
# Create symbolic link for storage
php artisan storage:link
\`\`\`

### 6. Start Development Server

**Option A: Using Laravel Herd (Recommended)**

If you have [Laravel Herd](https://herd.laravel.com) installed, the site will automatically be available at:
\`\`\`
http://laravel_api.test
\`\`\`

**Option B: Using Artisan**

\`\`\`bash
php artisan serve
\`\`\`

Visit: http://127.0.0.1:8000

### 7. Compile Frontend Assets

\`\`\`bash
# For development (with hot reload)
npm run dev

# For production
npm run build
\`\`\`

## Quick Setup Script

Run all setup commands at once:

\`\`\`bash
composer install && \
npm install && \
cp .env.example .env && \
php artisan key:generate && \
touch database/database.sqlite && \
php artisan migrate && \
php artisan storage:link && \
npm run build
\`\`\`

## Environment Variables

Key environment settings in \`.env\`:

\`\`\`env
APP_NAME=Laravel
APP_ENV=local
APP_DEBUG=true
APP_URL=http://laravel_api.test

DB_CONNECTION=sqlite

SESSION_DRIVER=file
CACHE_STORE=file
QUEUE_CONNECTION=sync
\`\`\`

## Common Issues

### Error: "No application encryption key"

**Solution:**
\`\`\`bash
php artisan key:generate
\`\`\`

### Error: "Database does not exist"

**Solution:**
\`\`\`bash
touch database/database.sqlite
php artisan migrate
\`\`\`

### Error: "Permission denied" (storage/logs)

**Solution:**
\`\`\`bash
chmod -R 775 storage bootstrap/cache
\`\`\`

### Frontend assets not loading

**Solution:**
\`\`\`bash
npm run build
\`\`\`

## API Endpoints

Document your API endpoints here. Example:

\`\`\`
GET    /api/users         - List all users
POST   /api/users         - Create user
GET    /api/users/{id}    - Get user
PUT    /api/users/{id}    - Update user
DELETE /api/users/{id}    - Delete user
\`\`\`

## Testing

\`\`\`bash
# Run tests
php artisan test

# Run tests with coverage
php artisan test --coverage
\`\`\`

## Tech Stack

- **Backend:** Laravel 12
- **Frontend:** Vue 3, Inertia.js
- **Database:** SQLite (development)
- **Styling:** Tailwind CSS

## Contributing

1. Fork the repository
2. Create your feature branch (\`git checkout -b feature/amazing-feature\`)
3. Commit your changes (\`git commit -m 'Add some amazing feature'\`)
4. Push to the branch (\`git push origin feature/amazing-feature\`)
5. Open a Pull Request

## License

This project is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).

## Author

**Luciano Nicacio**
- GitHub: [@LucianoNicacio](https://github.com/LucianoNicacio)
- Email: luciano.english@gmail.com
- LinkedIn: [linkedin.com/in/luciano-nicácio](https://linkedin.com/in/luciano-nicácio)
