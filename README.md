# Laravel API

A RESTful API built with Laravel 12 and SQLite.

## Requirements

- PHP 8.2+
- Composer
- SQLite

## Local Setup Instructions

### 1. Clone the Repository

\`\`\`bash
git clone git@github.com:LucianoNicacio/laravel_api.git
cd laravel_api
\`\`\`

### 2. Install Dependencies

\`\`\`bash
composer install
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

## Quick Setup Script

Run all setup commands at once:

\`\`\`bash
composer install && \
cp .env.example .env && \
php artisan key:g
