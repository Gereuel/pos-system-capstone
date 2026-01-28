# 📁 `pos-system-capstone/` (Root Folder)

**Purpose:**
Main project container. This is what you open in VS Code and push to GitHub.

---

## 📄 `README.md`

**What:** Project documentation
**Use it for:**

* Project description
* Features
* Tech stack
* Setup instructions

**Example content:**

* “Web-based POS System for retail stores”
* “Features: sales, inventory, reports”

---

## 📄 `.gitignore`

**What:** Files Git should NOT track
**Use it for:**

* `node_modules/`
* `.env`
* build files

**Why:** Keeps your repo clean and secure.

---

## 📄 `package.json` (optional)

**What:** Node.js project config
**Use it when:**

* You use Express, Axios, etc.
* You want scripts like `npm start`

---

# 🗄️ `database/`

**Purpose:** All database-related files

---

### 📄 `schema.sql`

**Use for:**
Creating tables

```sql
CREATE TABLE products (
  id INT PRIMARY KEY,
  name VARCHAR(100),
  price DECIMAL(10,2),
  stock INT
);
```

---

### 📄 `seed.sql`

**Use for:**
Initial test data (sample products, users)

---

### 📁 `migrations/`

**Use for:**
Tracking database changes over time
(advanced but professional practice)

---

# 🖥️ `backend/`

**Purpose:** Server-side logic (business logic + database)

---

## 📁 `backend/src/config/`

### 📄 `db.js`

**Use for:**
Database connection (MySQL, MongoDB, etc.)

---

### 📄 `env.js`

**Use for:**
Loading environment variables

---

## 📁 `backend/src/controllers/`

**Purpose:** Handle requests and responses

| File                    | Use                      |
| ----------------------- | ------------------------ |
| `auth.controller.js`    | Login / logout           |
| `product.controller.js` | Add/edit/delete products |
| `sales.controller.js`   | Process transactions     |
| `report.controller.js`  | Sales summaries          |

**Rule:**
Controllers **do not** talk directly to HTML.

---

## 📁 `backend/src/models/`

**Purpose:** Database structure representation

| File           | Use               |
| -------------- | ----------------- |
| `User.js`      | Cashiers / admins |
| `Product.js`   | Items for sale    |
| `Sale.js`      | Transactions      |
| `Inventory.js` | Stock tracking    |

---

## 📁 `backend/src/routes/`

**Purpose:** URL endpoints

```js
GET /products
POST /sales
```

Each route calls a **controller**.

---

## 📁 `backend/src/middlewares/`

**Purpose:** Logic that runs before controllers

| File                 | Use              |
| -------------------- | ---------------- |
| `auth.middleware.js` | Check login      |
| `role.middleware.js` | Admin vs cashier |

---

## 📁 `backend/src/utils/`

**Purpose:** Helper logic

| File                  | Use             |
| --------------------- | --------------- |
| `receiptGenerator.js` | Create receipts |
| `validators.js`       | Validate inputs |

---

## 📄 `app.js`

**Use for:**
Register routes and middlewares

---

## 📄 `server.js`

**Use for:**
Start the server

---

# 🎨 `frontend/`

**Purpose:** User interface (what cashier sees)

---

## 📄 HTML Files

| File             | Use              |
| ---------------- | ---------------- |
| `index.html`     | Landing          |
| `login.html`     | Login screen     |
| `dashboard.html` | Overview         |
| `pos.html`       | Main POS screen  |
| `inventory.html` | Stock management |
| `reports.html`   | Sales reports    |

---

## 📁 `frontend/assets/css/`

**Purpose:** Styling

| File            | Use             |
| --------------- | --------------- |
| `main.css`      | Global styles   |
| `pos.css`       | POS layout      |
| `inventory.css` | Inventory page  |
| `reports.css`   | Charts & tables |

---

## 📁 `frontend/assets/js/`

**Purpose:** Page behavior

| File           | Use                |
| -------------- | ------------------ |
| `auth.js`      | Login logic        |
| `pos.js`       | Sales process      |
| `inventory.js` | Stock updates      |
| `reports.js`   | Charts             |
| `api.js`       | Fetch backend APIs |

---

## 📁 `frontend/components/`

**Purpose:** Reusable HTML parts

| File           | Use            |
| -------------- | -------------- |
| `navbar.html`  | Top navigation |
| `sidebar.html` | Menu           |
| `modal.html`   | Popups         |

---

# 🧪 `tests/`

**Purpose:** Testing

* Backend logic
* Frontend functionality

(Optional for school, impressive for portfolio)

---

# 📚 `docs/`

**Purpose:** Documentation & evidence

| Item                   | Use              |
| ---------------------- | ---------------- |
| `system-overview.md`   | How system works |
| `api-documentation.md` | Endpoints        |
| `erd.png`              | Database diagram |
| `screenshots/`         | UI proof         |

---

# 📄 `.env.example`

**Purpose:**
Template for environment variables

```env
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=
```

---

## ✅ How You Should Use This (Beginner Flow)

1. Build **HTML + CSS first**
2. Add **JS logic**
3. Connect frontend to backend
4. Add database
5. Document in `docs/`