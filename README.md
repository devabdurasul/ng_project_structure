# Angular Project Structure

A modern, scalable Angular application structure following best practices for large-scale applications.

![Angular](https://img.shields.io/badge/Angular-20.1.0-DD0031?style=flat&logo=angular)
![TypeScript](https://img.shields.io/badge/TypeScript-5.8.2-3178C6?style=flat&logo=typescript)
![RxJS](https://img.shields.io/badge/RxJS-7.8.0-B7178C?style=flat&logo=reactivex)

## 📋 Overview

This repository demonstrates a recommended project structure for Angular applications, emphasizing:

- Standalone components architecture
- Feature-based organization
- Separation of concerns
- Scalability
- Maintainability
- Code reusability

Perfect for medium to large-scale applications or as a starting point for new projects.

## 🚀 Features

- **Core**: Application-wide singleton services, interceptors, and guards
- **Features**: Self-contained business domains with their own standalone components, services, and routes
- **Shared**: Reusable standalone components, directives, pipes, and models
- **Layouts**: Flexible layout templates for different sections of the application
- **Modern Angular Practices**: Latest Angular version fully embracing standalone components
- **SCSS Styling**: Structured stylesheet organization

## 🏗️ Project Structure

```
src/
├── app/
│   ├── core/                  # Singleton services and application-wide utilities
│   │   ├── config/            # App configuration
│   │   ├── guards/            # Route guards
│   │   ├── interceptors/      # HTTP interceptors
│   │   └── services/          # Core services (auth, logging, etc.)
│   │
│   ├── features/              # Feature areas (business domains)
│   │   ├── auth/              # Authentication feature
│   │   │   ├── pages/         # Auth pages (login, register)
│   │   │   └── services/      # Auth-specific services
│   │   │
│   │   ├── dashboard/         # Dashboard feature
│   │   │   ├── components/    # Dashboard-specific components
│   │   │   ├── pages/         # Dashboard pages
│   │   │   └── services/      # Dashboard-specific services
│   │   │
│   │   └── orders/            # Orders feature
│   │       ├── components/    # Order-specific components
│   │       ├── pages/         # Order pages (list, details, edit)
│   │       └── services/      # Order-specific services
│   │
│   ├── layouts/               # Application layout templates
│   │   ├── admin-layout/      # Layout for authenticated sections
│   │   └── public-layout/     # Layout for public sections
│   │
│   └── shared/                # Shared functionality across features
│       ├── components/        # Reusable UI components
│       ├── directives/        # Custom directives
│       ├── models/            # Shared data models/interfaces
│       ├── pipes/             # Custom pipes
│       └── utils/             # Utility functions
│
├── assets/                    # Static assets
│   ├── fonts/                 # Font files
│   └── images/                # Image files
│
├── environments/              # Environment configurations
└── styles/                    # Global styles
```

## 🛠️ Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/devabdurasul/ng_project_structure.git
   cd ng-project-structure
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm start
   ```

4. Open your browser and navigate to `http://localhost:4200/`

## 📝 Usage

### Development Server

```bash
npm start
```

### Building for Production

```bash
npm run build
```

### Running Tests

```bash
npm test
```

### Code Scaffolding

Generate new components, services, etc. using Angular CLI:

```bash
ng generate component shared/components/my-component --standalone
ng generate service features/orders/services/order
```

## 🧩 Architecture Principles

This project structure follows these key principles:

1. **Component-Based Architecture**: Each feature is organized around standalone components
2. **Separation of Concerns**: Clear boundaries between different parts of the application
3. **Reusability**: Shared components and services for maximum code reuse
4. **Scalability**: Structure supports growth without becoming unwieldy
5. **Maintainability**: Organized code that's easier to understand and maintain

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Angular Documentation](https://angular.dev/)
- [Angular Style Guide](https://angular.dev/style-guide)
