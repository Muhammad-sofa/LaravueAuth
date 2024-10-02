# LaravueAuth Web Application
This is a simple web application built with PHP Laravel and Vue.js. The app includes basic authentication features such as login and registration with form validation and error handling.

## Features
- User registration and login
- Client-side validation using Vue.js
- Server-side validation using Laravel

## Setup Instructions LaravueAuth
1. Clone the repository.
2. Run `composer install` to install PHP dependencies.
3. Set up your `.env` file for database configuration.
4. Run `php artisan migrate` to set up the database.
5. Run `npm install` and `npm run dev` to compile assets.
6. Start the server with `php artisan serve`.

## Code Structure
- `resources/js/components`: Vue components for login and registration.
- `app/Http/Controllers`: Laravel controllers for handling authentication logic.

## Run Laravue
- Open browser and access http://127.0.0.1:8000/register for registration.
- Access http://127.0.0.1:8000/login for login.
