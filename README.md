# Tugas Akhir Teknologi Web 2023

## Instalation

### Init DB

-   Create DB Name: hotel
    or via terminal

```
mysql -u root -p
```

- enter your db credential

```
create database hotel;
exit;
```

### Init Commands:

```
cp .env.example .env // after that start filling credential at .env

composer install
npm install
npm run dev
php artisan migrate:fresh --seed
php artisan serv                => Terminal 1
php artisan reverb:start     => Terminal 2   //run the websocket server for realtime notification
```

### Development build

```
npm run dev
```

### Production Build

```
npm run build
```

### Login:

-   Email: gavriel.k.adi12@gmail.com
-   Password: gavriel
