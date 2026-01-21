# 💰 Finance Dashboard API (Django REST Framework)

Finance Dashboard API — **Django REST Framework (DRF)** asosida ishlab chiqilgan shaxsiy moliyaviy boshqaruv tizimi. Ushbu loyiha frontend (Web / Mobile) ilovalar bilan ishlash uchun **to‘liq REST API** taqdim etadi.

API foydalanuvchilarga kirim–chiqimlarni boshqarish, balansni nazorat qilish, kategoriyalar bo‘yicha tahlil qilish va **JWT token** orqali xavfsiz autentifikatsiyadan foydalanish imkonini beradi.

---

## 🎯 Loyiha maqsadi

Ushbu API foydalanuvchiga:

* daromad va xarajatlarni API orqali qo‘shish
* qayerga qancha pul ketayotganini ko‘rish
* real vaqtda balansni hisoblash
* JWT orqali xavfsiz login qilish
* profil va parolni boshqarish
* frontend (React / Vue / Mobile) bilan ishlash

imkonini beradi.

---

## ⚙️ O‘rnatish (Installation)

```bash
git clone https://github.com/Jurayev-Marat/8_imtihon_DRF.git
cd 8_imtihon_DRF
python -m venv venv
venv\Scripts\activate  # Linux/Mac: source venv/bin/activate
pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

Server ishga tushgach:

```
http://127.0.0.1:8000/
```

---

## 🔐 Authentication (JWT) Ro'yxatdan o'tish uchun kod terminalga keladi 

API **JWT (JSON Web Token)** asosida ishlaydi.

### 🔑 Auth endpointlar

| Method | Endpoint             | Tavsif                         |
| ------ | -------------------- | ------------------------------ |
| POST   | /auth/signup/        | Ro‘yxatdan o‘tish              |
| POST   | /auth/login/         | Login (access + refresh)       |
| POST   | /auth/token/refresh/ | Access token yangilash         |
| POST   | /auth/logout/        | Logout (refresh token bilan)   |
| POST   | /auth/forgot/        | Parolni tiklash (kod yuborish) |
| POST   | /auth/reset/         | Yangi parol o‘rnatish          |
| PUT    | /auth/update/        | Profilni yangilash             |

### 📌 Himoyalangan endpoint chaqirish

```http
Authorization: Bearer ACCESS_TOKEN
```

---

## 👤 Foydalanuvchi (Users & Profile)

* Signup / Login
* JWT token orqali autentifikatsiya
* Profil ma’lumotlarini ko‘rish
* Profilni tahrirlash (ism, avatar)
* Parolni almashtirish

---

## 💵 Kirim (Income API)

### Endpointlar

| Method | Endpoint               | Tavsif             |
| ------ | ---------------------- | ------------------ |
| GET    | /finance/incomes/      | Kirimlar ro‘yxati  |
| POST   | /finance/incomes/      | Kirim qo‘shish     |
| GET    | /finance/incomes/{id}/ | Kirim detail       |
| PUT    | /finance/incomes/{id}/ | Kirimni tahrirlash |
| DELETE | /finance/incomes/{id}/ | Kirimni o‘chirish  |

* To‘lov turlari: **cash / card / dollar**
* Kirim qo‘shilganda balans avtomatik oshadi

---

## 💸 Chiqim (Expense API)

### Endpointlar

| Method | Endpoint                | Tavsif              |
| ------ | ----------------------- | ------------------- |
| GET    | /finance/expenses/      | Chiqimlar ro‘yxati  |
| POST   | /finance/expenses/      | Chiqim qo‘shish     |
| GET    | /finance/expenses/{id}/ | Chiqim detail       |
| PUT    | /finance/expenses/{id}/ | Chiqimni tahrirlash |
| DELETE | /finance/expenses/{id}/ | Chiqimni o‘chirish  |

* Chiqim qo‘shilganda balansdan avtomatik ayiriladi

---

## 🗂 Kategoriyalar (Categories API)

* Kirim va chiqim kategoriyalari alohida
* Har bir kategoriya foydalanuvchiga bog‘langan
* Kategoriya bo‘yicha jami summa hisoblanadi

### Endpointlar

| Method | Endpoint                  | Tavsif                |
| ------ | ------------------------- | --------------------- |
| GET    | /finance/categories/      | Kategoriyalar         |
| POST   | /finance/categories/      | Kategoriya qo‘shish   |
| PUT    | /finance/categories/{id}/ | Kategoriya tahrirlash |
| DELETE | /finance/categories/{id}/ | Kategoriya o‘chirish  |

---

## 💰 Balans (Balance Logic)

* Har bir foydalanuvchi uchun alohida balans
* Balans tarkibi:

  * Naqd
  * Karta
  * Dollar
* Dollar → so‘m kursi bilan hisoblanadi
* Kirim / Chiqim qo‘shilganda avtomatik yangilanadi

---

## 📊 Dashboard API

* Kun / oy / yil bo‘yicha filtr
* Sana oralig‘i bo‘yicha filter
* Jami kirim
* Jami chiqim
* Umumiy balans
* Kategoriya bo‘yicha statistika
* Grafiklar uchun JSON ma’lumotlar

---

## 📄 API Dokumentatsiya

* Swagger UI:

```
/swagger/
```

* ReDoc:

```
/redoc/
```

---

## 🛠 Texnologiyalar

* **Backend:** Django, Django REST Framework
* **Auth:** SimpleJWT
* **Database:** SQLite
* **Docs:** drf-spectacular (Swagger / ReDoc)
* **Media:** Django Media Files

---

## 📂 Loyiha tuzilmasi

```
conf/
finance/
users/
shared/
manage.py
requirements.txt
README.md
```

---

## ✅ Xulosa

Finance Dashboard API — bu:

* real loyiha
* to‘liq REST API
* JWT bilan himoyalangan
* frontend va mobile uchun tayyor

🎓 **DRF imtihon / portfolio uchun ideal loyiha**

---

Agar xohlasangiz:

* Postman collection
* API diagramma
* React frontend

hammasini ulab beraman.
