# 🛡️ Advanced Bootstrap 5 Form Validation System

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Bootstrap Version](https://img.shields.io/badge/Bootstrap-5.3.0-purple.svg)](https://getbootstrap.com/)
[![Language](https://img.shields.io/badge/Language-HTML/JS-orange.svg)](#)

Ushbu loyiha **Asilbek2706** tomonidan ishlab chiqilgan bo'lib, u foydalanuvchi ma'lumotlarini kiritishda xatoliklarni oldini olish uchun ilg'or **Client-side Validation** (mijoz tomonidagi tekshiruv) tizimini namoyish etadi.



## 🎯 Loyihaning maqsadi
Asosiy maqsad — foydalanuvchi interfeysini (UI) intuitiv qilish va noto'g'ri ma'lumotlar serverga yuborilishidan oldin ularni filtrlash. Bu tizim elektron tijorat saytlari va ro'yxatdan o'tish sahifalari uchun ideal yechimdir.

## 🚀 Texnik imkoniyatlar
* **Real-time Validation:** `was-validated` klassi yordamida foydalanuvchi xatosini darhol vizual ko'rsatish.
* **Custom Feedback:** Har bir maydon uchun alohida `valid-feedback` va `invalid-feedback` xabarlari.
* **Input Group Integration:** Foydalanuvchi nomi (username) uchun `@` belgisi bilan integratsiya qilingan input-group validation.
* **Conditional Logic:** To'lov usullari va manzillar uchun radio-tugmalar va chekboxlar tizimi.
* **Security Mindset:** Xavfsiz to'lov shakllari (CVV, Expiration date) uchun tayyor maskalar va validatsiya maydonlari.

## 🛠 Ishlatilgan texnologiyalar
| Texnologiya | Vazifasi |
| :--- | :--- |
| **HTML5** | Semantik struktura va form elementlari |
| **Bootstrap 5** | Grid tizimi, UI komponentlar va CSS utilitalari |
| **JavaScript (ES6)** | Formani yuborishni to'xtatish va validatsiya logikasi |

## 📂 Koddan namunalar

### JavaScript Validatsiya Logikasi
Ushbu skript formadagi barcha majburiy maydonlarni tekshiradi va agar xatolik bo'lsa, formani yuborishni (`submit`) bloklaydi:

```javascript
(function() {
    'use strict'
    var forms = document.querySelectorAll('.needs-validation')
    Array.prototype.slice.call(forms).forEach(function(form) {
        form.addEventListener('submit', function(event) {
            if (!form.checkValidity()) {
                event.preventDefault()
                event.stopPropagation()
            }
            form.classList.add('was-validated')
        }, false)
    })
})()
