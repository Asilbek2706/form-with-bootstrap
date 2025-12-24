# Bootstrap 5 Tooltip Validation (No JavaScript)

Ushbu loyiha **Bootstrap 5** yordamida shakllantirilgan, faqat **CSS** orqali ishlaydigan validatsiya (tasdiqlash) tizimini namoyish etadi. Bunda hech qanday JavaScript kodidan foydalanilmagan.

## 🚀 Xususiyatlari

* **JS-siz Validatsiya:** Brauzerning standart `:invalid` va `:focus` pseudo-klasslari yordamida ishlaydi.
* **Tooltip uslubi:** Xatolik xabarlari Bootstrap-ning `invalid-tooltip` klassi orqali chiroyli dizaynda ko'rinadi.
* **Responsive Dizayn:** Mobil va desktop qurilmalar uchun to'liq moslashuvchan.
* **Zamonaviy UI:** Toza va sodda billing (to'lov) formasi.

---

## 🛠 Ishlatilgan texnologiyalar

* **HTML5** - Forma strukturasi uchun.
* **Bootstrap 5.3** - Tayyor komponentlar va grid tizimi uchun.
* **Custom CSS** - Tooltip-larni faqat xatolik bo'lganda va fokus tushganda ko'rsatish uchun.

---

## ⚙️ Qanday ishlaydi?

Asosiy mantiq CSS-dagi quyidagi selektorlar orqali amalga oshirilgan:

```css
/* Tooltipni boshlang'ich holatda yashirish */
.form-control:invalid ~ .invalid-tooltip,
.form-select:invalid ~ .invalid-tooltip {
    display: none;
}

/* Input xato bo'lsa va unga fokus berilsa, tooltipni ko'rsatish */
input:focus:invalid ~ .invalid-tooltip,
select:focus:invalid ~ .invalid-tooltip {
    display: block;
    top: 100%;
    z-index: 5;
}
