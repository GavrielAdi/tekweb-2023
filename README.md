# Tugas Akhir Teknologi Web 2024

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

## Modul

-   Dashboard
    -   Guests Chart
    -   Guests on this day

-   Transaction
    -   Payment
        -   Create & Store Payment
        -   Payment History
    -   Room Reservation
        -   Step:
            1. Choose Customer:
                - Create New Customer / Pick from existing Customer
            2. Input Form:
                - How many people
                - Date for Check In
                - Date for Check Out
            3. Pick Available Room:
                - Check unoccupied room between date Check in and Check out.
                - Room Capacity must be > than input how many people.
            4. Confirmation & Down Payment
                - Down Payment: 15% of total price
                - Payment must be equal or higher than Down Payment
            5. If the transaction Success:
                - Send Email notification to Super Role about transaction payment.
                - Send push notification to Super Role.
                - Update all dashboard view

-   CUSTOMER Management
    -   Create Customer
    -   Read Customer
        -   Paginate
        -   Search
    -   Update Customer
    -   Delete Customer
        -   Cannot be deleted if the customer has transaction
    -   Customer Detail

-   USER Management
    -   Create User
    -   Read User (Super, Admin)
        -   Paginate
        -   Search
    -   Read User (Customer)
        -   Paginate
        -   Search
    -   Update User
    -   Delete User
        -   Cannot be deleted if the User has transaction
    -   User Detail

-   ROOM Management
    -   Create Room
    -   Read Room
        -   Paginate
        -   Search
    -   Update Room
    -   Delete Room
        -   Cannot be deleted if the Room already connected in transaction
    -   Room Detail

-   CRUD ROOM TYPE
    -   Create Room Type
    -   Read Room Type
        -   Paginate
        -   Search
    -   Update Room Type
    -   Delete Room Type

-   CRUD ROOM STATUS
    -   Create Room Status
    -   Read Room Status
        -   Paginate
        -   Search
    -   Update Room Status
    -   Delete Room Status

## Reservation Plot

-   Customer Register to Admin
-   Fill in customer's identity (based on KTP)
    -   Fill in by the Admin
-   Book a room (how much people? and when?)
    -   Fill in by the Admin based on customers order
        -   rooms are recommended by the system based on the input value.
-   Choose the room
    -   Fill in by the Admin based on customers order
        -   Choose based on room type, price, and facility.
-   Make a down payment
    -   Fill in by the Admin based on minimum down payment (15% of total price)
-   Stay
-   Finish (Check Out) and pay the insufficient payment

## Laravel License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).