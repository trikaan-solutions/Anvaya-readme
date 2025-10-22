# Anvaya CMS

## 🧱 Overview

Anvaya CMS is a **SaaS platform** built using **Ruby on Rails**, designed for modular, secure, and scalable application management. The project is developed and maintained by **Trikaan Dev Team**.

---

## ⚙️ Core Features

* **Single-Tenant Architecture**: Built for a single organization with modular feature expansion.
* **Admin Panel**: Central control for managing users, roles, and feature access.
* **Feature-based Access**: Enable or disable features per user role or plan.
* **Audit Logging**: All system and user actions (including custom events) are logged for transparency.
* **Secure Sessions & Secrets**: Rails credentials and cookies use the latest security standards.
* **Future Chat Integration**: ActionCable + Redis-based chat module.

---

## 🧩 Tech Stack

* **Backend:** Ruby on Rails 8 (PostgreSQL)
* **Frontend:** TailwindCSS (via `tailwindcss-rails`)
* **Auth:** Devise (customized for role-based authentication)
* **Audit Logging:** `audited` gem with support for domain events
* **Database:** PostgreSQL

---

## 🚀 Setup Instructions

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/trikaan-solutions/anvaya-cms.git
cd anvaya-cms
```

### 2️⃣ Install Dependencies

```bash
bundle install
yarn install --check-files
```

### 3️⃣ Setup the Database

```bash
bin/rails db:create db:migrate db:seed
```

This seeds the database with:

* Default Plans (Basic, Pro, Enterprise)
* A default Admin user and base configurations

### 4️⃣ Start the Server

```bash
bin/dev
```

Visit the app at: `http://localhost:3000`

---

## 🧠 Application Architecture

```
app/
 ├── controllers/
 │   ├── admin/
 │   ├── users/
 │   └── public/
 ├── models/
 │   ├── user.rb
 │   ├── plan.rb
 │   ├── feature.rb
 │   └── audit_log.rb
 ├── views/
 └── middleware/
     └── custom_session_store.rb
```

---

## 🛡️ Security & Best Practices

* CSRF, XSS, and cookie tampering protection enabled.
* Strong session management with encrypted keys.
* All secrets stored using `Rails.application.credentials`.

---

## 🔍 Audit Logging

* Logs all CRUD actions via `audited` gem.
* Supports **custom domain events** like Purchase Orders, Vehicle Inspections, etc.

---

## 📦 Future Enhancements

* ✅ Role-based Permission Engine
* ✅ Feature Toggles per Plan
* ✅ Admin Analytics Dashboard
* ✅ Real-time Chat System
* ✅ React Integration (optional frontend)

---

## 👨‍💻 Authors

**Trikaan Dev Team** — Core Development, Architecture & Product Management

---

## 🧭 Next Steps

* [ ] Finalize role-based permissions
* [ ] Add admin feature control dashboard
* [ ] Implement event-based audit logging
* [ ] Prepare React SPA integration

---

**📘 License:** MIT
