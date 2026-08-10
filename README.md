<div align="center">

# 🍽️ Restaurant Order Management System

![Flutter](https://img.shields.io/badge/Frontend-Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Language-Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)
![Supabase](https://img.shields.io/badge/Backend-Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/Database-PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)

> A centralized, cloud-integrated digital platform designed to facilitate the entire restaurant order lifecycle from preparation to payment.

</div>

---

## 📖 About The Project

In the contemporary food and beverage industry, the shift toward digitized operational workflows has become essential to maintain competitiveness and ensure high standards of service. Traditional manual or paper-based order tracking often leads to communication bottlenecks, delayed preparation times, and increased risks of administrative errors during the payment phase.

To address these challenges, this project introduces a mobile-first, cloud-integrated platform. The system tracks real-time updates across multiple stages of an order's progression—from the initial "Pending" status, through the culinary preparation phase, to the serving stage, and finally, payment processing. This ensures that restaurant staff can monitor table-specific demands with high accuracy and minimal latency.

---

## ✨ Core Modules & Features

The application is structured to optimize the efficiency of front-of-house and back-of-house operations with a clean, high-contrast monochrome UI design:

| Icon | Feature | Description |
| :---: | :--- | :--- |
| 📋 | **Menu List Management** | <ul><li>Provides conditional tab-based filtering (All, Food, Drink) to reduce user cognitive load.</li><li>Supports CRUD operations (Add, Edit, Delete) with a validation-first approach ensuring name, price, and category are properly defined.</li><li>Utilizes real-time Supabase synchronization (INSERT, UPDATE, DELETE) to update the catalog across the platform immediately.</li></ul> |
| 🪑 | **Orders Dashboard** | <ul><li>Central dashboard for staff to monitor real-time dining operations.</li><li>Displays at-a-glance details such as table number, unique order ID, accumulated total, and visual status indicators (Pending, Preparing, Served, Paid).</li><li>Features a "+ New Order" floating action button for rapid order initiation.</li></ul> |
| 📝 | **New Order Creation** | <ul><li>Interactive procurement form with dynamic state management.</li><li>Auto-calculates the "Estimated Total" in real-time as users select or deselect items via checkboxes.</li><li>Creates linked records in the `orders` and `order_items` tables upon submission.</li></ul> |
| 🔄 | **Order Lifecycle Tracking** | <ul><li>Granular management view to transition orders through predefined lifecycle stages (Pending, Preparing, Served) via an "Update Status" modal.</li><li>Includes a context-aware delete action that is only permitted during early stages to prevent erroneous cancellations after production begins.</li></ul> |
| 💳 | **Secure Payment Processing** | <ul><li>Transitions the primary action button to "Process Payment" once an order reaches the "Served" status.</li><li>Requires explicit staff validation to proceed, preventing accidental status changes.</li><li>Locks the order state to "Paid" in the database, rendering historical transaction data immutable.</li></ul> |

---

## 🛠️ Technology Stack

This system was engineered using modern, robust frameworks and tools:

| Component | Technology | Description |
| :--- | :--- | :--- |
| **Frontend Framework** | `Flutter` | Enables a single codebase to produce a responsive application functioning consistently across web and mobile platforms. |
| **Programming Language** | `Dart` | An object-oriented language selected for its high performance and seamless integration with Flutter. |
| **Backend & Database** | `Supabase` & `PostgreSQL` | A Backend-as-a-Service (BaaS) providing a scalable relational database, real-time subscriptions, and secure API endpoints. |
| **API Integration** | `Supabase Flutter SDK` | Acts as the intermediary bridge for data retrieval and modification between the app and the cloud database. |
| **Development Environment**| `Visual Studio Code` | Served as the primary IDE due to its extensive plugin ecosystem and robust debugging tools. |

---

## 🏛️ Development Architecture

The development followed a systematic approach to ensure reliability and responsiveness:
1. **Project Initialization:** Configured the Flutter environment and initialized the Supabase client for a secure, authenticated channel.
2. **Database Schema:** Designed a robust relational schema with an `orders` table to track global state and an `order_items` table to handle specific menu selections.
3. **Model Implementation:** Engineered an Order data model bridging raw database JSON to application objects, using strict null-safety mechanisms to prevent runtime crashes.
4. **Service Layer:** Developed an `OrderService` class encapsulating all database interactions using asynchronous programming to keep the UI responsive.

---

## 👨‍💻 Developer Information

| Profile | Name | Matric Number | Course |
| :---: | :--- | :--- | :--- |
| 👩‍💻 | **Jeanette Hauw Chandra** | `X25EC3020` | SECP3106-02 - APPLICATION DEVELOPMENT |

<div align="center">
  <i>Presented for: Dr. Seah Choon Sen | Faculty of Computing | Universiti Teknologi Malaysia</i>
</div>
