# Smart Retail - E-Commerce Platform

A feature-rich e-commerce web application built with Angular 16, Bootstrap 5, and TypeScript. This project provides a complete online shopping experience with customer and admin portals.

![Angular](https://img.shields.io/badge/Angular-16.2.0-red)
![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3.3-purple)
![TypeScript](https://img.shields.io/badge/TypeScript-5.1.3-blue)
![License](https://img.shields.io/badge/license-MIT-green)

## 📋 Table of Contents
- [Features](#features)
- [Technologies](#technologies)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Development Server](#development-server)
- [Build](#build)
- [Testing](#testing)
- [Project Structure](#project-structure)
- [Contributing](#contributing)

## ✨ Features

### 🛍️ Customer Portal
- **Product Catalog**: Browse products with dynamic search functionality
- **Product Details**: Detailed product views with specifications
- **Shopping Cart**: Add/remove items, update quantities
- **Wishlist**: Save favorite products
- **User Profile**: Manage personal information and preferences
- **Order Management**: View order history and track orders
- **Invoice Generation**: Download PDF invoices using jsPDF and html2canvas
- **Address Book**: Save and manage multiple delivery addresses
- **Secure Payment**: Integrated payment processing
- **Responsive Design**: Mobile-friendly interface with Bootstrap 5

### 🔧 Admin Portal
- **Dashboard**: Overview of store metrics and activities
- **Product Management**: Add, edit, and delete products
- **Stock Management**: Monitor and update inventory levels
- **Order Processing**: Manage customer orders
- **Protected Routes**: Secure admin access with route guards

## 🛠️ Technologies

- **Frontend Framework**: Angular 16.2.0
- **UI Library**: Bootstrap 5.3.3
- **Icons**: Bootstrap Icons
- **PDF Generation**: jsPDF 2.5.2
- **Canvas Rendering**: html2canvas 1.4.1
- **State Management**: RxJS 7.8.0
- **Language**: TypeScript 5.1.3
- **Build Tool**: Angular CLI 16.2.16

## 📦 Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js**: v16.x or higher ([Download](https://nodejs.org/))
- **npm**: v8.x or higher (comes with Node.js)
- **Angular CLI**: v16.2.16
  ```bash
  npm install -g @angular/cli@16.2.16
  ```

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/smart-retail.git
   cd smart-retail
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Verify installation**
   ```bash
   ng version
   ```

## 💻 Development Server

Run the following command to start the development server:

```bash
ng serve
```

or

```bash
npm start
```

Navigate to `http://localhost:4200/` in your browser. The application will automatically reload if you change any of the source files.

### Development with custom port:
```bash
ng serve --port 4300
```

### Development with host binding:
```bash
ng serve --host 0.0.0.0
```

## 🏗️ Build

### Development Build
```bash
ng build --configuration development
```

### Production Build
```bash
ng build
```

or

```bash
npm run build
```

The build artifacts will be stored in the `dist/ecommerce-project` directory. The production build is optimized with:
- Code minification
- Tree shaking
- Output hashing for cache busting
- Bundle size: Maximum 10MB (configured in angular.json)

### Watch Mode
For continuous building during development:
```bash
npm run watch
```

## 🧪 Testing

### Running Unit Tests

Execute the unit tests via [Karma](https://karma-runner.github.io):

```bash
ng test
```

or

```bash
npm test
```

The test runner will launch Chrome and execute all spec files.

### Running End-to-End Tests

```bash
ng e2e
```

**Note**: You need to first add a package that implements end-to-end testing capabilities (e.g., Protractor, Cypress, or Playwright).

## 📁 Project Structure

```
smart-retail/
├── src/
│   ├── app/
│   │   ├── admin-dashboard/        # Admin portal components
│   │   │   ├── add-product/
│   │   │   ├── edit-product/
│   │   │   └── manage-stock/
│   │   ├── user-profile/           # User profile components
│   │   │   ├── my-details/
│   │   │   ├── my-orders/
│   │   │   │   └── invoice/
│   │   │   └── account-settings/
│   │   ├── guards/                 # Route guards
│   │   ├── homepage/               # Landing page
│   │   ├── product-detail/         # Product details page
│   │   ├── cart/                   # Shopping cart
│   │   ├── wishlist/               # Wishlist
│   │   ├── address/                # Address management
│   │   ├── payment/                # Payment processing
│   │   ├── login/                  # Authentication
│   │   ├── admin-login/            # Admin authentication
│   │   ├── app-routing.module.ts   # Application routes
│   │   ├── app.component.ts        # Root component
│   │   └── app.module.ts           # Root module
│   ├── assets/                     # Static assets
│   ├── index.html                  # Main HTML file
│   ├── main.ts                     # Application entry point
│   └── styles.css                  # Global styles
├── angular.json                    # Angular CLI configuration
├── package.json                    # Project dependencies
├── tsconfig.json                   # TypeScript configuration
├── web.config                      # IIS deployment config
└── README.md                       # This file
```

## 🗺️ Application Routes

| Route | Component | Description |
|-------|-----------|-------------|
| `/` | Homepage | Landing page with product listings |
| `/product/:id` | Product Detail | Individual product view |
| `/cart` | Cart | Shopping cart |
| `/wishlist` | Wishlist | Saved items |
| `/address` | Address | Address management |
| `/payment` | Payment | Payment processing |
| `/login` | Login | User authentication |
| `/profile/details` | My Details | User profile |
| `/profile/orders` | My Orders | Order history |
| `/profile/settings` | Settings | Account settings |
| `/admin-login` | Admin Login | Admin authentication |
| `/admin-dashboard/*` | Admin Dashboard | Admin portal (protected) |

## 🔐 Authentication & Guards

The application implements route guards for security:

- **LoginGuard**: Prevents navigation away from login during authentication
- **AdminLoginGuard**: Protects admin routes from unauthorized access

## 🎨 Code Scaffolding

Generate new components, services, and more:

```bash
# Component
ng generate component component-name

# Service
ng generate service service-name

# Module
ng generate module module-name

# Directive
ng generate directive directive-name

# Pipe
ng generate pipe pipe-name

# Guard
ng generate guard guard-name

# Interface
ng generate interface interface-name

# Class
ng generate class class-name

# Enum
ng generate enum enum-name
```

## 🌐 Deployment

### IIS Deployment
The project includes a `web.config` file for IIS hosting with proper Angular routing configuration.

### Other Platforms

**Netlify/Vercel:**
- Build command: `ng build`
- Publish directory: `dist/ecommerce-project`

**Firebase:**
```bash
ng build
firebase deploy
```

## 📜 Available Scripts

| Script | Command | Description |
|--------|---------|-------------|
| `start` | `ng serve` | Start development server |
| `build` | `ng build` | Build for production |
| `watch` | `ng build --watch --configuration development` | Build in watch mode |
| `test` | `ng test` | Run unit tests |

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Author

Your Name - [@Anshuman Singh Yadav](https://github.com/yanshuman)

## 🙏 Acknowledgments

- Generated with [Angular CLI](https://github.com/angular/angular-cli) version 16.2.16
- UI components from [Bootstrap 5](https://getbootstrap.com/)
- Icons from [Bootstrap Icons](https://icons.getbootstrap.com/)


## 📚 Further Help

To get more help on the Angular CLI:
- Use `ng help`
- Check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page
- Visit [Angular Documentation](https://angular.io/docs)

---

⭐ **Star this repository if you find it helpful!**
