# Laravel Installation on Windows 10

This guide will walk you through installing Laravel on Windows 10, setting up a local development environment, and creating your first Laravel project.

## Prerequisites

Make sure the following prerequisites are installed on your machine:

- [PHP](https://www.php.net/downloads) (version 7.3 or higher)
- [Composer](https://getcomposer.org/download/) (Dependency Manager for PHP)
- [XAMPP](https://www.apachefriends.org/index.html) or [WAMP](https://www.wampserver.com/) (for local server setup)

---

## Steps to Get Started with Laravel on Windows 10

### 1. Install PHP

1. Download the latest PHP version for Windows from [PHP Downloads](https://www.php.net/downloads).
2. Extract the downloaded ZIP file and add the PHP folder to your system's PATH variable:
   - Search for "Environment Variables" in the Windows search bar.
   - Select **Environment Variables** and then **Path** under System Variables.
   - Add the path to your PHP folder (e.g., `C:\php`).

3. Verify the installation by running `php -v` in the Command Prompt. You should see the PHP version if it’s installed correctly.

### 2. Install Composer

1. Download the latest Composer setup file from [Composer Download](https://getcomposer.org/download/).
2. Run the installer and follow the instructions, making sure Composer is available globally on your PATH.

3. Verify the installation by running `composer -v` in the Command Prompt.

### 3. Set Up a Local Server (XAMPP or WAMP)

1. Download and install either XAMPP or WAMP to set up a local server.
2. Start the Apache server using the XAMPP/WAMP control panel.

### 4. Create a New Laravel Project

1. Open the Command Prompt and navigate to the directory where you want to create your Laravel project.
2. Run the following command to create a new Laravel project:

   ```bash
   composer create-project --prefer-dist laravel/laravel projectname
   ```

   Replace `projectname` with your desired project folder name.

3. Navigate into the project directory:

   ```bash
   cd projectname
   ```

### 5. Start the Laravel Development Server

1. In the Command Prompt, start the Laravel development server:

   ```bash
   php artisan serve
   ```

2. Open a web browser and go to `http://127.0.0.1:8000` to view your Laravel application.

---

## Additional Configuration

### Database Setup

1. Open the `.env` file in your Laravel project folder.
2. Configure your database connection settings (e.g., `DB_DATABASE`, `DB_USERNAME`, `DB_PASSWORD`).

### Running Migrations

1. To create the necessary tables, run the following command:

   ```bash
   php artisan migrate
   ```

---

## Common Commands

Here are some helpful Laravel commands to get you started:

- `php artisan make:model ModelName -m`: Create a model and migration.
- `php artisan make:controller ControllerName`: Create a new controller.
- `php artisan make:migration migration_name`: Create a migration.
- `php artisan migrate`: Run all pending migrations.

---

## Additional Resources

- [Laravel Documentation](https://laravel.com/docs)
- [Composer Documentation](https://getcomposer.org/doc/)
