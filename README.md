# Recipe Management System (RMS) 🍽️
### Full-Stack MERN Gourmet Food & Culinary Recipe Platform with Geolocation & Ingredients Inspection

Welcome to the **Recipe Management System (RMS)**! A modern, full-stack application developed with **React 18, Node.js, Express, and MongoDB**, styled with **Tailwind CSS**.

---

## 🌟 Key Features Implemented

1. **🔐 Multi-Role Authentication:**
   - **Admin Login:** Dedicated Administrator Console (`admin@recipemaster.com` / `Admin@12345`).
   - **User Login & Sign Up:** Registration, login, and session persistence.
   - Quick auto-fill helper buttons for instant testing without typing.

2. **📍 Location Logo & Area Checker:**
   - Dedicated location pin logo placed directly beside the search bar.
   - Click to open the **Delivery Area Checker Modal**.
   - Search any metropolitan area or pincode (e.g. `10001`, `10002`, `Downtown`) to check serviceability, delivery fees, and arrival times.

3. **🔍 Real-Time Search & Multi-Filters:**
   - Search recipes by title, ingredients, cuisine, or description.
   - Category filter pills: *All, Italian, Indian, Mexican, Asian, Healthy, Dessert, Fast Food*.
   - Dietary badges: *Vegetarian, Vegan, Gluten-Free, Halal, Non-Veg*.
   - Sorting options: *Recommended, Top Rated, Price Low-to-High, Price High-to-Low*.

4. **🍲 Food Cards:**
   - High-definition food photography with smooth zoom hover effects.
   - Dietary indicator dots (Pure Veg vs. Non-Veg).
   - Food title, description, star rating, and formatted price.
   - **❤️ Wishlist Heart Button:** Save favorite recipes with badge count.
   - **🛒 Add to Cart Button:** Instant addition with item counter.
   - **⚡ Buy Now Button:** 1-Click quick checkout.

5. **🥕 Interactive Ingredients & Recipe Inspection Modal:**
   - **Clicking any food card** reveals the complete list of ingredients with exact quantities (e.g., 1.5 cups Arborio Rice, 250g Mushrooms).
   - **Interactive Pantry Checklist:** Cross off ingredients you already have at home!
   - Step-by-step cooking procedures with numbered badges.
   - Macro-nutritional table: Calories, Protein, Carbs, Fats, and Fiber.
   - Executive chef pro tips and advice.

6. **🛍️ Cart & Direct "Buy Now" Checkout:**
   - Slide-over cart drawer with quantity counters (+ / -) and price breakdown.
   - Direct Buy Now checkout modal for single-dish purchases.
   - Delivery address form and payment selection (Online UPI, Card, Cash on Delivery).
   - Instant order placement with unique generated Order ID (e.g., `ORD-94812`).

7. **⚡ Admin Management Dashboard:**
   - Add new recipes to MongoDB with custom ingredients, prices, images, and steps.
   - View, update, or delete existing dishes.
   - Live incoming customer order queue with status updater (*Order Placed*, *Preparing*, *Out for Delivery*, *Delivered*).
   - Delivery hub coverage overview.

8. **📞 Contact Page & Inquiries:**
   - Professional inquiry form with instant confirmation feedback.
   - Headquarters address, hotlines, operating hours, and FAQ accordion.

9. **📜 Footer & Official Copyright Certificate:**
   - Complete site navigation, social channels, and legal notices.
   - **Copyright Certificate Viewer Modal:** Displays an official digital Certificate of Registration (Reg No: `RMS-CR-2026-884920-INT`) with cryptographic signature and printable format.

10. **📊 Project Presentation (PPT) & Comprehensive Documentation:**
    - Interactive 14-slide presentation slide deck (`presentation/index.html`).
    - Presentation script & slide outline (`presentation/RECIPE_MANAGEMENT_SYSTEM_PPT.md`).
    - 25+ page IEEE software documentation (`docs/PROJECT_DOCUMENTATION.md`).
    - Styled HTML documentation reader (`docs/DOCUMENTATION_VIEWER.html`).

---

## 🚀 How to Run the Project

### Option A: Instant Browser Mode (Zero Installation Required!)
You can launch and test the entire project **immediately in any web browser**:
1. Open the project folder:
   ```
   C:\Users\SriMu\.gemini\antigravity\scratch\recipe-management-system\
   ```
2. Double-click **`index.html`** (or open with Chrome, Edge, or Opera).
3. The React 18 client starts instantly with pre-loaded recipes, simulated MongoDB storage, interactive modals, search, location checker, cart, buy now, admin portal, and copyright certificate!

---

### Option B: Full-Stack MERN Production Mode (Node.js + Express + MongoDB)
When you have Node.js and MongoDB installed on your system:

#### 1. Start the Backend API Server:
```bash
cd backend
npm install
npm run seed     # Populates MongoDB with initial recipes, users, and locations
npm start        # Starts Express server on http://localhost:5000
```

#### 2. Start the Frontend React App:
```bash
cd ../frontend
npm install
npm run dev      # Starts Vite React dev server on http://localhost:3000
```

---

## 🔑 Demo Credentials

| Role | Email | Password | Access Level |
| :--- | :--- | :--- | :--- |
| **Administrator** | `admin@recipemaster.com` | `Admin@12345` | Full Admin Console, Recipe CRUD, Orders Management |
| **Demo User** | `user@recipemaster.com` | `User@12345` | Customer Cart, Wishlist, Buy Now Orders |

*(Tip: In the login modal, you can simply click the **"⚡ Auto-Fill"** button to load these credentials automatically!)*

---

## 📂 Project Structure

```
recipe-management-system/
├── index.html                           # One-click browser runnable React SPA
├── README.md                            # Complete project guide and documentation
│
├── backend/                             # Express & Node.js API with MongoDB
│   ├── package.json
│   ├── server.js                        # Express server entry point
│   ├── .env                             # Port, MongoDB URI, JWT Secret
│   ├── config/
│   │   └── db.js                        # MongoDB Mongoose connection
│   ├── models/
│   │   ├── User.js                      # User schema with bcrypt password hashing
│   │   ├── Recipe.js                    # Recipe schema with ingredients & nutrition
│   │   ├── Order.js                     # Customer orders schema
│   │   └── Location.js                  # Delivery areas & serviceable hubs
│   ├── routes/
│   │   ├── authRoutes.js                # Login, signup, admin-login, wishlist
│   │   ├── recipeRoutes.js              # Recipe search, filter, CRUD
│   │   ├── orderRoutes.js               # Order placement and tracking
│   │   └── locationRoutes.js            # Area serviceability checker
│   ├── middleware/
│   │   └── authMiddleware.js            # JWT protection & adminOnly guard
│   └── seed/
│       └── seedData.js                  # Database seeder script
│
├── frontend/                            # React 18 frontend
│   ├── index.html                       # Standalone browser React distribution
│   ├── package.json                     # Vite/React configuration
│   ├── vite.config.js
│   └── src/
│       ├── App.jsx
│       ├── main.jsx
│       └── services/
│           └── api.js                   # REST API client connecting to backend
│
├── presentation/                        # Project Presentation & Slide Deck (PPT)
│   ├── index.html                       # Interactive 14-slide animated presentation deck
│   └── RECIPE_MANAGEMENT_SYSTEM_PPT.md  # Slide transcript & speaker viva notes
│
└── docs/                                # Project Documentation
    ├── PROJECT_DOCUMENTATION.md         # 25+ page IEEE software report & architecture
    └── DOCUMENTATION_VIEWER.html        # Styled HTML documentation reader & PDF exporter
```

---

## 🎓 Viva & Evaluation Checklist

- [x] **Project Name:** Recipe Management System
- [x] **Admin Login:** Secured portal at `/admin` or via modal switch
- [x] **User Login & Signup:** With password hashing and JWT
- [x] **Location Logo & Area Checker:** Interactive header icon to verify delivery zones
- [x] **Search Bar:** Real-time search across titles, descriptions, and ingredients
- [x] **Food Item Cards:** HD image, description, price, rating, and dietary tags
- [x] **Wishlist:** Saved recipes with header badge counter
- [x] **Add to Cart & Buy Now:** Cart drawer with counter & 1-click quick checkout
- [x] **Ingredients Inspection:** Clicking any dish opens full ingredients list & measurements
- [x] **Pages:** Home Page, Contact Page, Admin Page, Modals
- [x] **Footer:** Multi-column links & ISO compliance notes
- [x] **Copyright Certificate:** Official registration dialog with Reg No: `RMS-CR-2026-884920`
- [x] **MongoDB Storage:** Data modeled with Mongoose collections
- [x] **Presentation (PPT):** Interactive slide deck in `presentation/index.html`
- [x] **Project Documentation:** Complete software specification in `docs/PROJECT_DOCUMENTATION.md`
