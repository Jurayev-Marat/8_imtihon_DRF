# 💰 Finance Dashboard (Django)

**Finance Dashboard** — Django framework asosida ishlab chiqilgan **shaxsiy moliyaviy boshqaruv tizimi**.  
Loyiha foydalanuvchilarga **kirim va chiqimlarni boshqarish**, **balansni nazorat qilish**, **kategoriyalar bo‘yicha tahlil qilish** va **ko‘p tilli interfeys**dan foydalanish imkonini beradi.

---

## 🎯 Loyiha maqsadi

Bu loyiha foydalanuvchiga:
- o‘z daromad va xarajatlarini yozib borish
- qayerga qancha pul ketayotganini ko‘rish
- real vaqtda balansni bilish
- profil va parolni boshqarish
- 3 xil tilda (UZ / RU / EN) ishlash

imkonini beradi.
---

## ⚙️ O‘rnatish (Installation)

```bash
git clone https://github.com/USERNAME/finance-dashboard.git
cd finance-dashboard
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver




---

## 🚀 Asosiy imkoniyatlar (Features)

### 👤 Foydalanuvchi (Auth & Profile)
- Ro‘yxatdan o‘tish (Signup)
- Login / Logout
- Parolni tiklash (email orqali tasdiqlash kodi bilan)
- Yangi parol o‘rnatish
- Profilni tahrirlash (avatar, ma’lumotlar)
- Profil ichida parolni almashtirish
- Django `messages` orqali xabarlar

---

### 🌍 Ko‘p tilli tizim (Internationalization)
- 3 ta til qo‘llab-quvvatlanadi:
  - 🇺🇿 O‘zbek
  - 🇷🇺 Русский
  - 🇬🇧 English
- `{% trans %}`, `gettext`, `gettext_lazy` ishlatilgan
- `.po / .mo` fayllar orqali tarjima
- Tilni sahifa ichidan almashtirish

---

### 💵 Kirim (Income)
- Kirim kategoriyalarini yaratish
- Kirim kategoriyasini tahrirlash va o‘chirish
- Kirim qo‘shish
- Kirimni tahrirlash
- Kirimni o‘chirish
- To‘lov turlari:
  - Naqd
  - Karta
  - Dollar
- Kirim qo‘shilganda balans avtomatik oshadi

---

### 💸 Chiqim (Expense)
- Chiqim kategoriyalarini yaratish
- Chiqim kategoriyasini tahrirlash va o‘chirish
- Chiqim qo‘shish
- Chiqimni tahrirlash
- Chiqimni o‘chirish
- To‘lov turlari:
  - Naqd
  - Karta
  - Dollar
- Chiqim qo‘shilganda balansdan avtomatik ayiriladi

---

### 🗂 Kategoriyalar
- Kirim va chiqim kategoriyalari alohida
- Har bir kategoriya foydalanuvchiga bog‘langan
- Har bir kategoriya bo‘yicha jami summa hisoblanadi
- Kategoriya uchun rasm (icon) qo‘llab-quvvatlanadi

---

### 💰 Balans boshqaruvi
- Har bir foydalanuvchi uchun alohida balans
- Balans tarkibi:
  - Naqd
  - Karta
  - Dollar
- Dollar → so‘m kursi bilan hisoblash
- Balansni qo‘lda yangilash imkoniyati
- Umumiy balans formulasi:


---

### 📊 Dashboard
- Kunlik / haftalik / oylik filtr
- Sana oralig‘i bo‘yicha filtr
- Kirim va chiqim yig‘indisi
- Umumiy balans
- Kategoriyalar bo‘yicha statistika
- Grafiklar uchun tayyor ma’lumotlar

---

### 🎨 Dizayn (UI / UX)
- Dark mode 🌙 / Light mode ☀️
- Tema localStorage’da saqlanadi
- Responsive dizayn (Bootstrap 5)
- Sidebar navigatsiya
- Custom CSS dizayn

---

## 🛠 Texnologiyalar

- **Backend:** Django
- **Frontend:** HTML, CSS, Bootstrap 5
- **Database:** SQLite
- **Auth:** Django Authentication
- **i18n:** Django Internationalization
- **Email:** Django `send_mail`

---

## 📂 Template tuzilmasi

templates/
├─ accound/
│ ├─ login.html
│ ├─ signup.html
│ ├─ forgot_password.html
│ ├─ reset_password.html
│ └─ profile.html
│
├─ base.html
├─ dashboard.html
├─ category_list.html
├─ category_detail.html
├─ add_category.html
├─ update_category.html
├─ delete_category.html
├─ add_income.html
├─ delete_income.html
│
├─ expense_category_list.html
├─ expense_category_detail.html
├─ add_expense_category.html
├─ delete_expense_category.html
├─ add_expense.html
└─ delete_expense.html
