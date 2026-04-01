# MM Finance Web Portal
## www.mnsnbfc.com

---

## 📁 Folder Structure

```
mnsnbfc/
├── index.html                          ← Homepage (Public)
├── css/
│   ├── style.css                       ← Main site styles
│   └── dashboard.css                   ← Admin & customer dashboard styles
├── pages/
│   ├── admin/
│   │   └── dashboard.html              ← Admin Panel (login: admin / admin123)
│   └── customer/
│       └── portal.html                 ← Customer Portal
└── README.md
```

---

## 🔐 Login Credentials

| Role     | Username | Password  | URL                              |
|----------|----------|-----------|----------------------------------|
| Admin    | admin    | admin123  | index.html → Admin Login button  |
| Customer | any email| any pass  | index.html → Customer Login      |

---

## ✅ Features Implemented

### Homepage (index.html)
- Fixed navbar with scroll effect
- Hero section with live portfolio preview card
- About Us section with stats
- Products section (6 loan/deposit products)
- EMI Calculator (interactive sliders)
- Investor Relations (with financial data table)
- Contact Us (form + contact info)
- Footer with RBI registration badge
- Admin Login modal
- Customer Login + Registration modal

### Admin Dashboard (pages/admin/dashboard.html)
- Sidebar navigation
- Dashboard with 4 KPI stat cards
- **Bar Chart** – Monthly loan disbursement (Chart.js)
- **Pie Chart** – Loan portfolio mix (Chart.js)
- **Line Chart** – Collection efficiency trend
- **Doughnut Chart** – Application status breakdown
- Recent loan applications table with Approve/Reject buttons
- **Loan Management** – Full table with filter/search
- **Credit Score Analysis** – Dynamic scoring engine with ring gauge
- **EMI Calculator** – With 12-month amortization schedule
- Customers directory
- Deposits & FD management
- Reports download section

### Customer Portal (pages/customer/portal.html)
- Overview dashboard (loans, EMI due, savings balance, FD)
- **Apply for Loan** – 4-step wizard (Loan details → Personal → Documents → Submit)
- **Application Status Tracker** – Step-by-step progress view
- **EMI Calculator** – With live calculation
- **My Account** – Savings account card + create new account
- **Deposit / FD** – Book FD with maturity calculator + view existing FDs

---

## 🌐 Deployment to mnsnbfc.com

### Option 1: Static Hosting (Recommended)
Upload all files to any static hosting:
- **Netlify**: Drag & drop folder → set custom domain → mnsnbfc.com
- **Vercel**: `vercel --prod` → add custom domain
- **GitHub Pages**: Push to repo → Settings → Pages → Custom domain

### Option 2: cPanel / Shared Hosting
1. Compress `mnsnbfc/` folder as ZIP
2. Login to cPanel → File Manager → public_html
3. Upload and extract ZIP
4. Point domain mnsnbfc.com → public_html

### Option 3: AWS / GCP
- Upload to S3 bucket → enable static website hosting
- Create CloudFront distribution → point mnsnbfc.com

### DNS Configuration
```
Type    Name    Value
A       @       <server-IP>
CNAME   www     mnsnbfc.com
```

---

## 🛠 Tech Stack
- Pure HTML5, CSS3, Vanilla JavaScript
- Chart.js (CDN) for dashboard charts
- Google Fonts: Playfair Display + DM Sans
- No backend required (extend with Node.js/PHP for production)

---

## 📌 Production Recommendations
1. Add real authentication (JWT / OAuth)
2. Connect to database (MySQL / MongoDB)
3. Integrate CIBIL API for real credit scores
4. Add payment gateway for EMI payments
5. Enable SSL certificate (Let's Encrypt)
6. Add RBI-mandated KYC (DigiLocker / Aadhaar API)
