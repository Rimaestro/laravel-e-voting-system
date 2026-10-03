# Laravel E-Voting System

A web application for managing a small, role-based election. The current code supports administrator and voter flows: candidate management, voter validation, ballot submission, and viewing election results.

## Features

- Laravel authentication and email verification
- Administrator and voter dashboards
- Candidate management, including candidate photos
- Voter validation by an administrator
- One recorded vote per validated voter
- Election result summaries

This is a learning application. Review its election rules, access controls, and operational security before using it for a real election.

## Stack

- PHP 8.2+
- Laravel 12
- SQLite or another database supported by Laravel
- Node.js and npm for frontend assets

## Local setup

    git clone https://github.com/Rimaestro/laravel-e-voting-system.git
    cd laravel-e-voting-system
    composer install
    npm install

Copy .env.example to .env and configure the database, then initialize the application:

    cp .env.example .env

    php artisan key:generate
    php artisan migrate --seed
    npm run build
    php artisan serve

Open http://127.0.0.1:8000. The seeder creates a generic development user; set its role and credentials locally before trying administrator-specific flows.

## Development

Run the Laravel test suite with:

    php artisan test

## Repository layout

- app/Http/Controllers/ — authentication, candidate, voter, and voting flows
- app/Models/ — election, candidate, voter, and vote records
- database/migrations/ — database schema
- resources/views/ — Blade interface
- routes/ — web and authentication routes
- tests/ — Laravel feature and unit tests

## License

See LICENSE, if present. If no license file is included, reuse and redistribution are not granted by this repository.

