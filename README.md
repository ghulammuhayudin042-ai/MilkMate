# MilkMate — Dairy Shop Management Software

A professional, fully responsive **React frontend** for managing a dairy shop selling milk, yogurt, lassi, cream, butter and desi ghee. Built as a 4-day frontend internship task — **frontend only, no backend**, powered by realistic mock data held in React state.

## Features

- **Dashboard** — today's sales/purchases/profit, total customers & products, pending payments, sales trend chart, product-sales split, payment-status split, recent sales, low-stock panel
- **Products** — catalog with categories (Milk, Yogurt, Lassi, Butter, Cream, Ghee, Other), add/edit/delete, product details with sales/purchase/stock history
- **Customers** — retail & wholesale customers, 360° profile view with a live **customer ledger** (debit/credit/running balance)
- **Sales / POS** — searchable product grid, cart with quantity controls, discount & payment capture, generates a printable **invoice**
- **Sales History** — searchable, filterable by payment status and date
- **Payments** — record payments against open invoices, auto-updates customer balances
- **Expenses** — categorized shop expenses with daily/monthly/total summaries
- **Stock Management** — opening/purchased/sold/returned/current stock, stock-in/out/adjustment/return movements
- **Suppliers & Purchases** — supplier directory, purchase recording, supplier ledgers
- **Employees** — team directory with roles (Admin, Manager, Salesman, Cashier)
- **Reports** — Sales, Purchases, Profit, Customers, Stock — each filterable by date range, customer, product and category
- **Categories, Notifications, Settings, Profile** — shop profile, invoice settings, currency, user account
- Fully responsive (desktop, tablet, mobile), with loading skeletons, empty states and confirm-on-delete dialogs throughout

## Tech Stack

React 18 · Vite · React Router 6 · Recharts · Lucide Icons · plain CSS (design tokens in `src/index.css`)

## Getting Started

```bash
npm install
npm run dev
```

Then open the printed local URL (typically `http://localhost:5173`).

To build a production bundle:

```bash
npm run build
npm run preview
```

## Demo Login

The login screen is frontend-only (no real authentication) — any email/password works, or use the pre-filled demo credentials:

- **Email:** admin@milkmate.pk
- **Password:** demo1234

## Project Structure

```
src/
  assets/
  components/
    common/      Button, Card, Modal, DataTable, Input, Select, SearchBar,
                  DatePicker, StatusBadge, EmptyState, Loading, Toaster...
    layout/       Layout, Sidebar, Header
    charts/       SalesOverviewChart, ProductSalesChart, PaymentStatusChart
  context/        AppContext.jsx — global app state (products, sales, customers, etc.)
  data/           mockData.js — all seed/demo data
  pages/          Dashboard, Products, Customers, Sales, Payments, Expenses,
                  Stock, Suppliers, Employees, Reports, Categories,
                  Notifications, Settings
  utils/          format.js — currency/date formatting helpers
  App.jsx         Route definitions
  main.jsx        App entry point
```

## Notes

- All data is **mock/demo data** held in React state (`src/data/mockData.js` + `AppContext`) — nothing is persisted to a backend or database, and a full page refresh resets it to the seed data.
- The app is ready for backend/API integration in a future phase: every data-mutating action already flows through a single `AppContext`, so swapping mock state for real API calls only touches that one file.

## Screenshots

Screenshots live in `screenshots/` — see `screenshots/README.md` for the exact filenames expected and quick capture steps. Once added, they'll show here:

| | |
|---|---|
| Login | ![Login](screenshots/login.png) |
| Dashboard | ![Dashboard](screenshots/dashboard.png) |
| Products | ![Products](screenshots/products.png) |
| Customers | ![Customers](screenshots/customers.png) |
| Sales / POS | ![Sales POS](screenshots/sales-pos.png) |
| Invoice | ![Invoice](screenshots/invoice.png) |
| Expenses | ![Expenses](screenshots/expenses.png) |
| Reports | ![Reports](screenshots/reports.png) |
| Settings | ![Settings](screenshots/settings.png) |
