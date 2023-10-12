# Technical Documentation

## Introduction

## Getting Started

### Prerequisites

- **PHP**: Version ^7.1.3
- **MySQL**: (Version not specified, but Laravel 5.7 supports MySQL >= 5.6)
- **Composer**: For managing PHP dependencies.
- **Git**: (Optional, for cloning the repository)

### Installation Steps

1. **Clone the Repository**

   ```bash
   git clone https://[bitbucket username]@bitbucket.org/the-restaurant-boss/the-restaurant-boss.git
   cd the-restaurant-boss
   ```

2. **Install Composer Dependencies**

   ```bash
   composer install
   ```

3. **Copy and Configure Environment Variables**

   ```bash
   cp .env.example .env
   ```

   Open `.env` and configure your application, database credentials, mail server, cache, and any other configurations.

4. **Generate Application Key**

   ```bash
   php artisan key:generate
   ```

   This will set the `APP_KEY` in your `.env` file, which is used for encryption.

5. **Run Database Migrations and Seeds**
   Ensure your database is running and the database credentials in `.env` are correct.

   ```bash
   php artisan migrate
   php artisan db:seed
   ```

   This will create the database structure and populate it with any seed data.

6. **Set Up Laravel Passport**

   ```bash
   php artisan passport:keys
   php artisan passport:install
   ```

   Note down the client ID and secret if you're using password grant types.

7. **Serve the Application**
   For development, you can use Laravel's built-in server:
   ```bash
   php artisan serve
   ```
   For production, you should set up a web server like Nginx or Apache. Ensure the web root is pointed to the `public` directory and the server is configured to hand off `.php` files to PHP-FPM.

## Codebase Overview

### Directory Structure

#### 1. `app/`

- **Models**: Defines the Eloquent models used in the application, representing and interacting with the database tables.
- **Controllers**: Manages application logic, handling HTTP requests and producing responses, often interacting with models.
- **Middleware**: Contains classes that can perform actions before and after HTTP requests enter the application.

#### 2. `routes/`

- **web.php**: Defines routes for web interface, typically returning views.
- **api.php**: Defines API routes, typically returning JSON.
- **console.php**: Defines routes for Artisan commands.

#### 3. `database/`

- **migrations/**: Contains files defining the database schema through Laravel’s Eloquent.
- **seeds/**: Contains seeders that can populate database tables with sample data.

#### 4. `tests/`

- **Unit/**: Contains tests that target a small, isolated portion of the code.
- **Feature/**: Contains tests that target larger areas, possibly interacting with the database or other services.

#### 5. `public/`

- **index.php**: The entry point for all requests to the application and configures autoloading.
- **assets/**: Contains compiled assets like CSS and JavaScript, as well as images and other public-facing files.

#### 6. `resources/`

- **views/**: Contains Blade templates that Laravel will compile and render as HTML.
- **lang/**: Contains translation files, allowing you to internationalize text in your application.
- **sass/**: Contains SASS that will be compiled to CSS.
- **js/**: Contains JavaScript files that might be compiled with Laravel Mix.

#### 7. `config/`

- Configuration files that allow you to define settings for database connections, email, caching, and various other aspects of Laravel applications.

#### 8. `storage/`

- **logs/**: Contains log files generated by the application.
- **app/**: Contains files generated during the operation of the application, like file uploads.
- **framework/**: Used for storing files generated by the framework like session, cache, and compiled view files.
- **oauth-private.key** and **oauth-public.key**: Contain the private and public keys used by Laravel Passport for API authentication.

#### 9. `bootstrap/`

- Contains the `app.php` file which bootstraps the framework and allows it to start serving responses.

### Key Components

## Models

### `User`

- `User.php`: Handles user-related data and operations.

### Overview

### Traits Used

1. `Notifiable`: Facilitates the sending of notifications to the user.
2. `SoftDeletes`: Enables the soft deletion of user records.
3. `HasApiTokens`: Manages API token functionalities, a part of Laravel Passport.
4. `HasRoles`: Administers roles and permissions of the user.

### Attributes

**Fillable**
Attributes that can be mass-assigned, safeguarding against mass-assignment vulnerabilities:

- `first_name`
- `last_name`
- `email`
- `password`
- `contact_id`
- `status`
- `api_token`
- `company`
- `role`
- `parent_id`
- `software_accounts`
- `ip_address`
- `last_logged_in`
- `from_demo`
- `partner_id`
- `last_active_date`
- `pagination_records_per_page`

### Relationships

### 1. `owner`

```php
return $this->belongsTo(\App\User::class);
```

- **Description**: Defines an inverse one-to-one relationship between `User` instances.
- **Return**: Returns a `belongsTo` relationship object, representing the owning `User` instance related to the current `User` instance.
- **SQL Queries**: Generates a SQL SELECT query to retrieve the related `User` instance based on the foreign key in the current `User` model instance.

### 2. `sub_users`

```php
return $this->hasMany(\App\User::class, 'owner_id', 'id');
```

- **Description**: Defines a one-to-many relationship between `User` instances, with `owner_id` as the foreign key.
- **Return**: Returns a `hasMany` relationship object, representing the collection of `User` instances where the current `User` instance is the owner.
- **SQL Queries**: Generates a SQL SELECT query to retrieve related `User` instances where `owner_id` matches the current `User` model's `id`.

### 3. `sub_user_restaurants`

```php
return $this->belongsToMany(\App\Restaurant::class, 'restaurant_accesses', 'user_id');
```

- **Description**: Many-to-many relationship between `User` and `Restaurant` via `restaurant_accesses`.
- **Return**: Returns a `belongsToMany` relationship object, representing a collection of `Restaurant` instances related to the current `User` instance through the `restaurant_accesses` pivot table.
- **SQL Queries**: Generates SQL SELECT queries to retrieve related `Restaurant` instances through the `restaurant_accesses` pivot table using the `user_id` foreign key.

### 4. `access_levels`

```php
return $this->hasMany('App\AccessLevel', 'user_id', 'id');
```

- **Description**: Defines a one-to-many relationship between `User` and `AccessLevel` using `user_id` as the foreign key.
- **Return**: Returns a `hasMany` relationship object, representing a collection of `AccessLevel` instances related to the current `User` instance.
- **SQL Queries**: Generates a SQL SELECT query to retrieve related `AccessLevel` instances where `user_id` matches the current `User` model's `id`.

### 5. `roles`

```php
return $this->belongsToMany(\App\Role::class, 'user_role');
```

- **Description**: Many-to-many relationship between `User` and `Role` via `user_role`.
- **Return**: Returns a `belongsToMany` relationship object, representing a collection of `Role` instances related to the current `User` instance through the `user_role` pivot table.
- **SQL Queries**: Generates SQL SELECT queries to retrieve related `Role` instances through the `user_role` pivot table.

### 6. `permissions`

```php
return $this->belongsToMany(\App\Permission::class, 'user_permission');
```

- **Description**: Many-to-many relationship between `User` and `Permission` via `user_permission`.
- **Return**: Returns a `belongsToMany` relationship object, representing a collection of `Permission` instances related to the current `User` instance through the `user_permission` pivot table.
- **SQL Queries**: Generates SQL SELECT queries to retrieve related `Permission` instances through the `user_permission` pivot table.

### 7. `restaurant_accesses`

```php
return $this->hasMany(\App\RestaurantAccess::class);
```

- **Description**: One-to-many relationship from `User` to `RestaurantAccess`.
- **Return**: Returns a `hasMany` relationship object, representing a collection of `RestaurantAccess` instances related to the current `User` instance.
- **SQL Queries**: Generates a SQL SELECT query to retrieve related `RestaurantAccess` instances where `user_id` matches the current `User` model's `id`.

### 8. `supplier`

```php
return $this->hasOne(\App\Supplier::class, 'user_id', 'id');
```

- **Description**: One-to-one relationship from `User` to `Supplier`.
- **Return**: Returns a `hasOne` relationship object, representing a single `Supplier` instance related to the current `User` instance.
- **SQL Queries**: Generates a SQL SELECT query to retrieve the related `Supplier` instance where `user_id` matches the current `User` model's `id`.

### 9. `supplier_location`

```php
return $this->hasOne(\App\SupplierLocation::class, 'user_id', 'id');
```

- **Description**: One-to-one relationship from `User` to `SupplierLocation`.
- **Return**: Returns a `hasOne` relationship object, representing a single `SupplierLocation` instance related to the current `User` instance.
- **SQL Queries**: Generates a SQL SELECT query to retrieve the related `SupplierLocation` instance where `user_id` matches the current `User` model's `id`.

### 10. `parent`

```php
return $this->belongsTo(\App\User::class, 'owner_id', 'id');
```

- **Description**: Inverse one-to-one relationship between `User` instances using `owner_id` as the foreign key.
- **Return**: Returns a `belongsTo` relationship object, representing the owning `User` instance related to the current `User` instance.
- **SQL Queries**: Generates a SQL SELECT query to retrieve the related owning `User` instance based on the foreign key in the current `User` model instance.

### 11. `child_users`

```php
return $this->hasMany(\App\User::class, 'owner_id', 'id');
```

- **Description**: One-to-many relationship from `User` to `User` (self-referential) using `owner_id` as the foreign key.
- **Return**: Returns a `hasMany` relationship object, representing a collection of `User` instances where the current `User` instance is the owner.
- **SQL Queries**: Generates a SQL SELECT query to retrieve related `User` instances where `owner_id` matches the current `User` model's `id`.

### 12. `child_users_location`

```php
return $this->hasManyThrough(\App\SupplierLocation::class, \App\User::class, 'owner_id', 'user_id', 'id', 'id');
```

- **Description**: Defines a has-many-through relationship from `User` through `User` to `SupplierLocation`, using `owner_id` as the foreign key.
- **Return**: Returns a `hasManyThrough` relationship object, representing a collection of `SupplierLocation` instances related to the current `User` instance through the `User` model.
- **SQL Queries**: Generates SQL SELECT queries to retrieve related `SupplierLocation` instances through the intermediary `User` model using `owner_id` and `user_id` as foreign keys.

### 13. `owner_user`

```php
return $this->belongsTo(\App\User::class, 'owner_id', 'id');
```

- **Description**: Inverse one-to-one relationship between `User` instances using `owner_id` as the foreign key.
- **Return**: Returns a `belongsTo` relationship object, representing the owning `User` instance related to the current `User` instance.
- **SQL Queries**: Generates a SQL SELECT query to retrieve the related owning `User` instance based on the foreign key in the current `User` model instance.

### 14. `restaurant`

```php
return $this->hasOne(\App\Restaurant::class, 'user_id', 'id');
```

- **Description**: One-to-one relationship from `User` to `Restaurant`.
- **Return**: Returns a `hasOne` relationship object, representing a single `Restaurant` instance related to the current `User` instance.
- **SQL Queries**: Generates a SQL SELECT query to retrieve the related `Restaurant` instance where `user_id` matches the current `User` model's `id`.

### 15. `child_users_location`

```php
return $this->hasManyThrough(\App\SupplierLocation::class, \App\User::class, 'owner_id', 'user_id', 'id', 'id');
```

- **Description**: Defines a has-many-through relationship from `User` through `User` to `SupplierLocation`, using `owner_id` as the foreign key.
- **Return**: Returns a `hasManyThrough` relationship object, representing a collection of `SupplierLocation` instances related to the current `User` instance through the `User` model.
- **SQL Queries**: Generates SQL SELECT queries to retrieve related `SupplierLocation` instances through the intermediary `User` model using `owner_id` and `user_id` as foreign keys.

### 16. `restaurant`

```php
return $this->hasOne(\App\Restaurant::class, 'user_id', 'id');
```

- **Description**: One-to-one relationship from `User` to `Restaurant`.
- **Return**: Returns a `hasOne` relationship object, representing a single `Restaurant` instance related to the current `User` instance.
- **SQL Queries**: Generates a SQL SELECT query to retrieve the related `Restaurant` instance where `user_id` matches the current `User` model's `id`.

### Methods

- `Restaurant.php`: Manages restaurant-related data and operations.
-

#### Controllers

- `UserController.php`: Manages user-related logic and HTTP request handling.
- `RestaurantController.php`: Manages restaurant-related logic and HTTP request handling.
-

## Database Schema

(TBD)

## API Documentation

(TBD )

## Testing

(TBD)

## Security

(TBD )