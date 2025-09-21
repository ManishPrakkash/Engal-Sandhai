# Engal Sandhai  

**Engal Sandhai** is a **web-based, intranet-only billing and realtime stock management system** built for a college campus vegetable store.  
It connects **faculty buyers (~300 daily active users)** with **admin faculty (5 users)** who manage daily stock and prices.  
The system generates bills, accepts static-QR-based payments (faculty upload payment screenshots), decrements stock **atomically**, and provides realtime stock updates across connected clients.  

---

## 📌 Quick Summary  
- **Single-server**, intranet-only web app for campus vegetable billing.  
- **Two roles**:  
  - **Admin (5 faculty)** → manage stock, prices, and orders.  
  - **Faculty (all others)** → place orders, upload payment screenshot, receive bills.  
- **Payment flow**:  
  - Static QR is displayed on the bill.  
  - Faculty uploads payment screenshot.  
  - Admin verifies payment manually.  
- **Stock updates**:  
  - Stock decrements only when payment screenshot is uploaded.  
  - Updates are processed **atomically** to prevent overselling.  
- **Realtime** updates via WebSockets.  

---

## 🚀 Key Features  
- 🔑 **Role-based authentication** (employee_id + password) with **forced password reset** option.  
- 🛠️ **Admin panel**:  
  - Add/update vegetables (photo, quantity, rate).  
  - View & filter orders.  
  - Verify/reject payments.  
  - Revert stock when needed.  
- 🛒 **Buying panel**:  
  - Browse vegetables with stock, price, and photo.  
  - Add to cart & place multi-item orders.  
  - Bill page with static admin QR.  
  - Upload payment screenshot.  
- 🔐 **Per-order session rule** → automatic logout after successful payment upload.  
- ⚡ **Realtime updates**:  
  - Stock updates across all connected faculty.  
  - New order notifications for admins.  
- 🧮 **Atomic multi-item order processing** → no overselling.  
- 🖼️ **Local file storage** for:  
  - Vegetable photos.  
  - Payment screenshots.  
- 🪶 **Lightweight, self-hosted stack** → no paid cloud required.
- 
---

## 🏗️ Tech Stack & Architecture  

### Frontend  
- ⚛️ React (Vite) + TypeScript  
- 🎨 Tailwind CSS  
- 🔄 React Router, Axios  
- 🔔 WebSocket client  

### Backend  
- 🔐 Firebase Authentication  
- 📂 Firestore Database  
- 📡 WebSockets for realtime updates  

---


