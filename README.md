# laravel-project

    sudo apt update
    sudo apt install php php-cli php-mysql php-mbstring php-xml php-curl unzip mysql-server composer -y
# Create the Database

    sudo mysql
    
    CREATE DATABASE my_laravel_db;
    CREATE USER 'dev_user'@'localhost' IDENTIFIED BY 'password123';
    GRANT ALL PRIVILEGES ON my_laravel_db.* TO 'dev_user'@'localhost';
    FLUSH PRIVILEGES;
    EXIT;

# install laravel requirement

    composer global require laravel/installer

# เพิ่ม PATH ให้ laravel

    echo 'export PATH="$HOME/.config/composer/vendor/bin:$PATH"' >> ~/.bashrc
    source ~/.bashrc
# เช็คอีกครั้ง

    laravel
# สร้าง Laravel Project

    laravel new lrv_erp_module
    
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

create file

/laravel_project/laravel_apps/resources/js/bootstrap.js

    import axios from 'axios';
    window.axios = axios;
    window.axios.defaults.headers.common['X-Requested-With'] = 'XMLHttpRequest';
    EOF
    
    npm install
    npm install axios
    npm run dev
    php artisan migrate

    composer require nwidart/laravel-modules
