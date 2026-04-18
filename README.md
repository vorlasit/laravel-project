# laravel-project

    sudo apt update
    sudo apt install php-cli php-curl php-mysql php-xml php-mbstring php-zip unzip mysql-server -y
# Install Composer

    curl -sS https://getcomposer.org/installer | php
    sudo mv composer.phar /usr/local/bin/composer

# Create the Database

    sudo mysql
    
    CREATE DATABASE my_laravel_db;
    CREATE USER 'dev_user'@'localhost' IDENTIFIED BY 'password123';
    GRANT ALL PRIVILEGES ON my_laravel_db.* TO 'dev_user'@'localhost';
    FLUSH PRIVILEGES;
    EXIT;

# create laravel project

    composer create-project laravel/laravel my-project-name
# Install Dependencies
Run this command to ignore the security advisories and install the framework packages:

    composer install --no-security-blocking

# Generate Application Key

    php artisan key:generate

# Run Migrations
Create your database tables in MySQL:

    php artisan migrate
# Launch the Server

    php artisan serve --host=0.0.0.0 --port=8000
# Install Laravel Breeze
Run these commands in your project directory to install the starter kit and its dependencies:

    sudo apt install npm
    npm install vite@^6.0.0 laravel-vite-plugin@^1.0.0 --save-dev
        
    composer require laravel/breeze --dev 
    php artisan breeze:install blade

Install frontend assets and migrate the database

    npm install
    npm run dev
    php artisan migrate
    
