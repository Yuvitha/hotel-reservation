# HotelMaster

A hotel reservation system built with Spring MVC, Apache Tiles, and PostgreSQL.

## Overview

HotelMaster is a web application for hotel room booking and management. Users can browse available rooms, make reservations, and manage their bookings. The application includes an admin panel for hotel staff to manage rooms, bookings, and user accounts.

## Technologies Used

- Java 11 with GraalVM
- Spring MVC 5.3
- Spring Security 5.7
- Apache Tiles 3.0
- PostgreSQL Database
- Maven Build System
- Bootstrap 3 CSS Framework
- jQuery

## Project Structure

```
src/main/java/hotelmaster/
├── account/           # User account management
├── admin/             # Admin panel controllers
├── booking/           # Room booking functionality
├── gallery/           # Photo gallery and room images
├── home/              # Homepage controller
├── notification/      # In-app notifications
├── rooms/             # Room management
└── util/              # Utility classes

src/main/webapp/
├── WEB-INF/
│   ├── layouts/       # Tiles layout definitions
│   └── views/         # JSP view templates
└── resources/         # Static assets (CSS, JS)
```

## Database Configuration

The application uses PostgreSQL. Database connection is configured via environment variables:
- `PGHOST`: Database host
- `PGDATABASE`: Database name
- `PGUSER`: Database username
- `PGPASSWORD`: Database password

## Running the Application

**Development Mode:**
The application runs using the embedded Tomcat 7 Maven plugin:
```
mvn tomcat7:run -Dmaven.tomcat.port=5000
```

**Production Deployment:**
The application is deployed using webapp-runner:
```
mvn clean package -DskipTests
java -jar target/dependency/webapp-runner.jar --port 5000 target/HotelMaster-1.0-SNAPSHOT.war
```

## Features

- **Room Browsing**: View available rooms with details and pricing
- **Room Search**: Search rooms by date range, price, and guest capacity
- **User Registration**: Create accounts and login
- **Facebook Login**: Social login integration
- **Room Booking**: Reserve rooms for specific dates
- **Admin Panel**: Manage rooms, bookings, and user accounts
- **Photo Gallery**: View room images
- **Contact Form**: Send inquiries to hotel staff

## Default Test Account

- Email: admin@hotelmaster.com
- Password: admin123

## Recent Changes

- **Feb 5, 2026**: Migrated from MySQL to PostgreSQL, upgraded Spring to 5.x for Java 11 compatibility, configured embedded Tomcat for Replit environment.

## Known Limitations

- Email functionality is disabled until SMTP credentials are configured
- Facebook login requires valid API credentials to be configured
