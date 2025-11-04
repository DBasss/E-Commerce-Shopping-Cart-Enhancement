<img width="1176" height="616" alt="image" src="https://github.com/user-attachments/assets/73adbd9a-fc4e-4988-9b7e-2bad8035fff0" /># Shopping Cart Enhancement - Thanksgiving Promotion System

## Overview
A full-stack e-commerce web application enhancement that implements a flexible discount management system for seasonal promotional campaigns. This project demonstrates end-to-end development from database design to user interface implementation.

## Features
- **Dynamic Discount System**: Configurable percentage-based discounts (20% Thanksgiving promotion on mobile products)
- **Product Management**: Admin interface for adding and managing product inventory
- **Visual Price Indicators**: Promotional badges, original vs. discounted pricing, and savings calculations
- **Smart Checkout**: Itemized discount breakdown showing subtotal, savings, and final total
- **Extensible Architecture**: Design patterns and SOLID principles for future promotional strategies

## Technologies Used
- **Backend**: Java, Servlet, JSP
- **Database**: MySQL
- **Server**: Apache Tomcat 9
- **IDE**: Eclipse IDE for Enterprise Java
- **Architecture**: MVC Pattern, DAO Pattern

## Project Structure
```
shopping-cart/
├── src/
│   ├── com.shashi.beans/         # Data models (ProductBean, UserBean, CartBean)
│   ├── com.shashi.service/        # Business logic interfaces
│   ├── com.shashi.service.impl/   # Service implementations
│   ├── com.shashi.srv/            # Servlets (LoginSrv, AddtoCart, etc.)
│   └── com.shashi.utility/        # Database utilities
├── WebContent/
│   ├── index.jsp                  # Homepage with product display
│   ├── userHome.jsp               # User dashboard
│   ├── cartDetails.jsp            # Shopping cart with discount breakdown
│   └── [other JSP pages]
└── databases/
    └── mysql_query.sql            # Database schema and sample data
```

## Key Enhancements

### 1. Database Schema Extension
- Added `discount` column to `product` table for flexible promotional pricing
- Supports percentage-based discounts (0-100%)

### 2. Backend Implementation
- **ProductBean**: Added discount field and `getDiscountedPrice()` calculation method
- **ProductServiceImpl**: Updated all CRUD operations to handle discount data
- Applied OOP principles for maintainable, extensible code

### 3. Frontend Enhancements
- Promotional "20% OFF" badges on qualifying products
- Dual pricing display (original struck-through + discounted price in red)
- Savings calculator showing exact amount saved
- Checkout page with transparent discount breakdown

## Setup Instructions

### Prerequisites
- Java JDK 8 or higher
- MySQL Server 8.0+
- Apache Tomcat 8.0+
- Eclipse IDE for Enterprise Java (or similar IDE)

### Installation Steps

1. **Clone the repository**
```bash
   git clone https://github.com/DBasss/shopping-cart-project.git
   cd shopping-cart-project
```

2. **Set up MySQL Database**
```sql
   CREATE DATABASE `shopping-cart`;
   USE `shopping-cart`;
   source databases/mysql_query.sql
```

3. **Configure Database Connection**
   - Open `src/application.properties`
   - Update database credentials:
```properties
     db.connectionString=jdbc:mysql://localhost:3306/shopping-cart
     db.username=root
     db.password=YOUR_PASSWORD
```

4. **Deploy to Tomcat**
   - Import project into Eclipse
   - Configure Tomcat 9 server in Eclipse
   - Right-click project → Run As → Run on Server

5. **Access the Application**
   - URL: `http://localhost:8080/shopping-cart/`
   - Admin Login: `admin@gmail.com` / `admin`
   - User Login: `guest@gmail.com` / `guest`

## Usage

### For Customers:
1. Browse products on the homepage
2. Products with discounts show "20% OFF" badges
3. Add items to cart
4. View cart to see discount breakdown
5. Proceed to checkout with discounted total

### For Admins:
1. Login with admin credentials
2. Access inventory management
3. Add new products with discount values (0-100%)
4. Update existing product discounts for promotions

## Technical Highlights

### Design Patterns Applied
- **MVC Pattern**: Separation of concerns (Model-View-Controller)
- **DAO Pattern**: Data access abstraction layer
- **Singleton Pattern**: Database connection management
- **Strategy Pattern**: Extensible discount calculation

### SOLID Principles
- **Single Responsibility**: Each class has one clear purpose
- **Open/Closed**: Discount system open for extension, closed for modification
- **Dependency Inversion**: Services depend on abstractions, not implementations

## Current Promotional Campaign
- **Products**: 5 mobile phones
- **Discount**: 20% off
- **Items**: iPhone 13 Pro, MOTOROLA G32, REDMI Note 12 Pro, Google Pixel 6a, iPhone 17

## Future Enhancements
- [ ] Promotional code system for coupon-based discounts
- [ ] Time-limited discounts with automatic start/end dates
- [ ] Tiered discounts (buy more, save more)
- [ ] Admin dashboard for visual discount management
- [ ] Email notifications for sale alerts

## Challenges Overcome
1. **Servlet Compatibility**: Resolved javax to jakarta namespace migration for Tomcat 9 compatibility
2. **Database Connection**: Debugged and configured MySQL connection with proper credentials
3. **Code Integration**: Updated multiple service methods without breaking existing functionality
4. **UI/UX Design**: Balanced promotional visibility with clean interface design

## Author
**Kevin Do**  
[LinkedIn](www.linkedin.com/in/kevin-do-570132327) | [Email](dokevin02@gmail.com)

## Acknowledgments
- Base project: [Original Shopping Cart Repository](https://github.com/shashirajraja/shopping-cart)
- Enhancement completed as part of coursework at [Clayton State University]


*This project demonstrates full-stack Java web development skills including database design, backend service implementation, frontend UI/UX enhancement, and production deployment.*
