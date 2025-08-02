# IOM ITB Frontend

A modern Vue.js web application for the Ikatan Orang Tua Mahasiswa (IOM) Institut Teknologi Bandung (ITB). This application serves as a platform for managing member registrations, donations, activities, and merchandise for the IOM ITB community.

## 🎯 About

IOM ITB (Ikatan Orang Tua Mahasiswa Institut Teknologi Bandung) is an organization that functions as a partner to ITB, specifically in fostering educational sustainability with a social and family-oriented approach. This frontend application provides a comprehensive platform for:

- Member registration and management
- Donation tracking and management
- Activity announcements and details
- Merchandise store
- Transaction management
- Help submissions

## ✨ Features

### 🏠 Home Page
- Organization overview and mission statement
- Latest donor information
- Recent activities showcase
- Statistical graphics and charts
- Video gallery

### 👥 Member Management
- Member registration forms
- Parent guardian registration
- Member data management

### 💰 Donation System
- Donation form with multiple payment methods
- Donation tracking and history
- QRIS payment integration
- Donor recognition

### 🎪 Activities
- Activity listings and details
- Activity registration
- Activity management

### 🛍️ Merchandise Store
- Product catalog
- Product details
- Shopping cart functionality
- Transaction processing

### 📋 Forms & Submissions
- Help request forms
- Various submission types
- Form validation

## 🛠️ Technology Stack

- **Frontend Framework**: Vue.js 3.4.27
- **State Management**: Vuex 4.0.0
- **Routing**: Vue Router 4.0.13
- **Styling**: Tailwind CSS 3.4.4
- **UI Components**: Flowbite Vue 0.1.5
- **HTTP Client**: Axios 1.7.2
- **Authentication**: JWT with vue-jwt-decode
- **Icons**: FontAwesome
- **Build Tool**: Vue CLI 5.0.8
- **Testing**: Vue Test Utils 2.0.0

## 📦 Installation

### Prerequisites
- Node.js (version 14 or higher)
- npm or yarn package manager

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd IOM-ITB-FE-main
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment Configuration**
   Create a `.env` file in the root directory and configure your environment variables:
   ```env
   VUE_APP_API_URL=your_backend_api_url
   VUE_APP_BASE_URL=your_base_url
   ```

4. **Run the development server**
   ```bash
   npm run serve
   ```
   The application will be available at `http://localhost:8080`

## 🚀 Available Scripts

- `npm run serve` - Start development server
- `npm run build` - Build for production
- `npm run test:unit` - Run unit tests

## 📁 Project Structure

```
src/
├── assets/           # Static assets (images, icons, videos)
├── components/       # Reusable Vue components
│   ├── button/      # Button components
│   ├── card/        # Card components
│   ├── form/        # Form components
│   ├── header/      # Header components
│   ├── input/       # Input components
│   ├── loading/     # Loading components
│   ├── navbar/      # Navigation components
│   └── table/       # Table components
├── router/          # Vue Router configuration
├── store/           # Vuex store modules
├── utils/           # Utility functions
├── views/           # Page components
│   ├── layout/      # Layout components
│   └── pages/       # Individual page components
├── css/             # Global styles
└── plugins/         # Vue plugins
```

## 🔧 Configuration

### Vue Configuration
The application uses a custom `vue.config.js` with webpack configuration for:
- Development server settings
- Polyfills for Node.js modules (crypto, stream, util)
- Buffer and process global variables

### API Integration
- Uses Axios for HTTP requests
- JWT-based authentication
- Cookie-based session management
- Accept-Language header support for internationalization

## 🎨 Styling

The application uses:
- **Tailwind CSS** for utility-first styling
- **Flowbite Vue** for pre-built components
- **DM Sans** font family
- Custom color scheme with main brand colors

## 🔐 Authentication

The application implements JWT-based authentication with:
- Token storage in cookies
- Automatic token refresh
- Protected routes
- User session management

## 📱 Responsive Design

The application is fully responsive and optimized for:
- Desktop computers
- Tablets
- Mobile devices

## 🧪 Testing

Run the test suite with:
```bash
npm run test:unit
```

## 🏗️ Building for Production

To build the application for production:
```bash
npm run build
```

The built files will be in the `dist/` directory.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👥 Team

This project is developed for IOM ITB (Ikatan Orang Tua Mahasiswa Institut Teknologi Bandung).

## 📞 Support

For support and questions, please contact the development team or create an issue in the repository.

---

**Note**: This application is designed to work with a corresponding backend API. Make sure the backend service is properly configured and running before using this frontend application.
