# 🛍️ E-Commerce 

This project is a **responsive e-commerce website** built using **Next.js 15 App Router**, **React Query**, **Redux**, and **Tailwind CSS**. It integrates with the [FakeStore API](https://fakestoreapi.com) to showcase product listings, filtering, cart functionality, and more.

## 🚀 Live Demo

👉 [Live Site on Vercel](https://e-commerce-dashboard-henna.vercel.app/)

---

## 📦 Features

### ✅ Core Requirements

1. **Product Listing Page**

   - Fetches and displays products from `https://fakestoreapi.com/products`
   - Shows image, title, price, and category
   - Clicking a product opens `/products/[id]`

2. **Filter by Category**

   - Categories fetched from `/products/categories`
   - Products can be filtered by selected category

3. **Product Detail Page**

   - Fetches details from `/products/:id`
   - Shows full info: title, image, price, description, rating, and category

4. **Add to Cart**

   - Add/remove items from cart
   - Cart count shown in header
   - `/cart` page displays all items, quantities, and total

5. **Add New Product (Simulated)**
   - `/add-product` page with form
   - Validated using `zod` + `react-hook-form`
   - Simulates POST request with success/fail toast

---

### 🌟 Bonus Features (Implemented)

- ✅ **Pagination** for product listing
- ✅ **Debounced Search**
- ✅ **Sorting by Price & Rating**
- ✅ **React Query** for fetching and caching
- ✅ **Redux Toolkit** for cart state
- ✅ **Responsive UI** with **Tailwind CSS**
- ✅ **Loader** and **Error handling UI**
- ✅ **Professional & accessible components**

---

## 🧠 Design Choices

| Area              | Decision                                                                |
| ----------------- | ----------------------------------------------------------------------- |
| **Framework**     | Next.js 15 (App Router) with Client Components where needed             |
| **State Mgmt**    | Redux Toolkit for Cart, React Query for fetching (decoupled & scalable) |
| **Styling**       | Tailwind CSS for speed, responsiveness, and utility-based styling       |
| **Form Handling** | `react-hook-form` with `zod` for type-safe validation                   |
| **UX/UI**         | Iconography via `@heroicons/react`, clean spacing, and mobile-first     |

---

## 📁 Project Structure

```
app/
  ├── page.tsx               # Product list
  ├── cart/page.tsx          # Cart
  ├── add-product/page.tsx   # Product form
  └── products/[id]/page.tsx # Product detail

components/
  ├── ui/                    # Reusable: Loader, ErrorMessage, Pagination, etc.
  ├── products/              # ProductCard, CategoryFilter, SortDropdown, Cart, ProductDetail, Products
  └── common/                # Navbar, etc.

hooks/                       # useProducts, useProductDetail, useCategories, useDebounce
lib/                         # store.ts, validators
slices/                      # cartSlice.ts
types/                       # Type definitions
```

---

## 🛠️ Setup Instructions

```bash
# 1. Clone the repo
git clone https://github.com/Rahulfordev/ecommerce-frontend.git
cd ecommerce-frontend

# 2. Install dependencies
yarn install
# or
npm install

# 3. Run the dev server
yarn dev
# or
npm run dev

# 4. Visit
http://localhost:3000
```

---

## 🔗 Dependencies

- **Next.js** (v15 App Router)
- **React Query** (tanstack)
- **Redux Toolkit**
- **Tailwind CSS**
- **React Hook Form + Zod**
- **Heroicons**
- **Toastify**
