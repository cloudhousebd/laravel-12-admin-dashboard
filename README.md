Laravel 12 Admin Dashboard — Cloud House Technologies
======================================================

Welcome to the Laravel 12 Admin Dashboard by Cloud House Technologies — a modular, scalable admin panel built with simplicity and robustness in mind.

This starter kit is crafted using Laravel 12, integrated with Laravel UI and Bootstrap 5, featuring ready-to-use authentication, a clean admin layout, and separated access control through guards.

------------------------------------------------------

FEATURES
--------

✅ Laravel 12 (Latest Stable)  
✅ User Authentication (Login, Register, Password Reset)  
✅ Laravel UI with Bootstrap 5 Styling  
✅ Separate Admin Guard with Custom Login  
✅ Role-Based Middleware Protection (Admin/User)  
✅ Modular Folder Structure for Scalability  
✅ Blade Components for Layout & Reuse  
✅ Clean Auth Redirection for Admin vs User  
✅ Secure Session & CSRF Protection  

------------------------------------------------------

FOLDER STRUCTURE HIGHLIGHTS
---------------------------

app/
├── Http/
│   ├── Controllers/
│   │   ├── Admin/        → Admin dashboard & auth
│   │   └── Auth/         → Default user authentication
├── Models/
│   ├── User.php
│   └── Admin.php         → Custom admin guard model

resources/
├── views/
│   ├── admin/            → Admin views
│   └── auth/             → Auth views (login, register, etc.)

routes/
├── web.php               → User routes
└── admin.php             → Admin-only routes

------------------------------------------------------

INSTALLATION GUIDE
------------------

1. Clone the Repo

   git clone https://github.com/cloudhouse/laravel-admin-dashboard.git
   cd laravel-admin-dashboard

2. Install PHP & JS Dependencies

   composer install
   npm install && npm run dev

3. Environment Setup

   cp .env.example .env
   php artisan key:generate

   (Then update your .env with DB and app info.)

4. Run Migrations

   php artisan migrate

5. Seed an Admin Account (Optional)

   php artisan tinker

   >>> \App\Models\Admin::create([
         'name' => 'Admin',
         'email' => 'admin@example.com',
         'password' => bcrypt('password'),
     ]);

6. Serve the App

   php artisan serve

   Visit:
   - User login → /login
   - Admin login → /admin/login

------------------------------------------------------

AUTHENTICATION & GUARDS
-----------------------

We use separate guards for users and admins:

- `web` → default users
- `admin` → admin-only routes

This ensures clear isolation of roles and easy expansion in the future.

------------------------------------------------------

TESTING ADMIN ACCESS
--------------------

Try accessing /admin without logging in — you’ll be redirected to /admin/login.

After successful login via the admin guard, you’ll be taken to the admin dashboard at /admin.

------------------------------------------------------

TECH STACK
----------

- PHP 8.2+
- Laravel 12.x
- Laravel UI (Bootstrap Auth Scaffolding)
- Blade Templating
- MySQL/PostgreSQL compatible
- Bootstrap 5

------------------------------------------------------

SUPPORT & CONTRIBUTION
----------------------

This script is maintained by Cloud House Technologies. For feature requests, issues, or contributions:

- Email: hello@cloudhousebd.com
- Website: https://cloudhousebd.com
- GitHub Issues: https://github.com/cloudhouse/laravel-12-admin-dashboard/issues

------------------------------------------------------

LICENSE
-------

This project is open-source under the MIT License. You're free to use, modify, and distribute.

© Cloud House Technologies 2025 — Smart Code. Real Impact.
