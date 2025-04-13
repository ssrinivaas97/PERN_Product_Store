# 🛍️ Full-Stack Product Management App

This is a fully functional full-stack web application for managing products, built with a modern tech stack including **Node.js**, **Express**, **React**, **Tailwind CSS**, **Zustand**, **Neon (PostgreSQL)**, and deployed on **AWS**. The app supports all CRUD operations with advanced features like rate limiting, bot protection, responsive UI, and theme customization.

## 🚀 Features

- Create, Read, Update, Delete (CRUD) for products
- Rate limiting and bot protection using **Arcjet**
- Global state management with **Zustand**
- Responsive UI with **Tailwind CSS** and **DaisyUI**
- Theme selection and persistence using local storage
- Optimized user experience with toast notifications and loading spinners
- Deployed on **AWS** using services like EC2, S3 (for assets), and PostgreSQL via **Neon**

## 🛠️ Tech Stack

### Backend
- **Node.js**, **Express.js**
- **Arcjet** middleware for rate limiting, bot detection, and protection against spoofed bots
- **Neon PostgreSQL** for production-ready, scalable relational database
- **Dotenv** for environment configuration
- **Axios** for HTTP requests

### Frontend
- **React**, **Vite**
- **Tailwind CSS**, **DaisyUI** for sleek UI
- **Zustand** for global state management
- **React Hot Toast** for notifications
- **React Router DOM** for routing
- **Lucide React** for modern icons

## 📡 API Endpoints

| Method | Endpoint                  | Description                     |
|--------|---------------------------|---------------------------------|
| GET    | `/api/products`           | Get all products                |
| GET    | `/api/products/:id`       | Get a specific product          |
| POST   | `/api/products`           | Create a new product            |
| PUT    | `/api/products/:id`       | Update an existing product      |
| DELETE | `/api/products/:id`       | Delete a product                |

## 💻 Frontend Highlights

- **Theme Selector**: Choose from multiple Tailwind DaisyUI themes
- **Navbar** with product count badge
- **Modals** for adding/editing products
- **Product Cards** with real-time updates
- **Routing** to individual product detail/edit pages

## 🧪 Running Locally

Follow these steps to set it up on a new machine:

### 1. Clone the Repo

\`\`\`bash
git clone https://github.com/your-username/product-management-app.git
cd product-management-app
\`\`\`

### 2. Install Backend Dependencies

\`\`\`bash
npm install
\`\`\`

### 3. Install Frontend Dependencies

\`\`\`bash
cd frontend
npm install
\`\`\`

### 4. Configure Environment Variables

Create a `.env` file in the root with:

\`\`\`
PORT=3000
DATABASE_URL=your_neon_db_connection_url
ARCJET_KEY=your_arcjet_key
\`\`\`

### 5. Seed the Database (Optional)

\`\`\`bash
cd backend/seeds
node products.js
\`\`\`

This will populate your database with demo products.

### 6. Run the App in Dev Mode

\`\`\`bash
# In the root folder
npm run dev
\`\`\`

### 7. Access the App

Open your browser at:

\`\`\`
Frontend: http://localhost:5173
Backend/API: http://localhost:3000/api/products
\`\`\`

## 🌍 Deployment

The app is configured for production deployment. When deployed to AWS (EC2/S3 for assets, Neon for DB):

- The React app is built and served statically from Express
- All frontend assets are bundled inside `/frontend/dist`
- Express serves both API and React SPA under the same domain

## 📷 Screenshots

> _[Add some screenshots here of the UI, mobile view, modals, etc.]_

## 🙏 Acknowledgements

- [Arcjet](https://arcjet.com/) for security middleware
- [Neon](https://neon.tech/) for managed PostgreSQL hosting
- [DaisyUI](https://daisyui.com/) + [Tailwind](https://tailwindcss.com/) for styling
- [Lucide Icons](https://lucide.dev/) for modern icons