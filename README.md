# 🎂 Person Age Calculator

A clean and minimal Age Calculator web app built with pure HTML, CSS, and JavaScript. Select your date of birth, click Calculate, and instantly get your exact age in **years, months, and days** — no page reload, no backend. Deployed live on Vercel.

![Demo](./Demo.png)

## 🌐 Live Demo

🔗 **[person-age-calculator.vercel.app](https://person-age-calculator.vercel.app)**

---

## ✨ Features

- 📅 **Date Picker Input** — Native HTML `<input type="date">` for smooth UX on all devices
- ⚡ **Instant Calculation** — Click "Calculate" and get result immediately with no page reload
- 🗓️ **Precise Output** — Displays exact age in **Years, Months, and Days**
- 🚫 **Future Date Validation** — Handles invalid or future date inputs gracefully
- 📱 **Fully Responsive** — Works on mobile, tablet, and desktop
- 🪶 **Ultra Lightweight** — Zero libraries, zero dependencies — pure vanilla JS

---

## 🗂️ Project Structure

```
Person-Age-Calculator/
│
├── index.html       # Date input, Calculate button, result display
├── style.css        # Card layout, input/button styling, responsive design
├── script.js        # calculateAge() — JavaScript Date logic
└── Demo.png         # Project preview screenshot
```

---

## ⚙️ How It Works

```
User selects Date of Birth via date picker
              ↓
Clicks "Calculate" button (calls calculateAge())
              ↓
JS gets today's date using new Date()
              ↓
Subtracts birth date from today's date
              ↓
Calculates exact Years, Months, and Days
              ↓
Result displayed in the #result paragraph
```

---

## 🧮 Calculation Logic

```javascript
function calculateAge() {
  const birthDate = new Date(document.getElementById("date").value);
  const today     = new Date();

  let years  = today.getFullYear()  - birthDate.getFullYear();
  let months = today.getMonth()     - birthDate.getMonth();
  let days   = today.getDate()      - birthDate.getDate();

  // Adjust for negative days / months
  if (days   < 0) { months--; /* borrow days from prev month */ }
  if (months < 0) { years--;  months += 12; }

  // Display result
  document.getElementById("result").innerHTML =
    `You are ${years} Years, ${months} Months, and ${days} Days old.`;
}
```

---

## 🛠️ Tech Stack

| Technology | Usage |
|------------|-------|
| **HTML5** | Date input, button, result paragraph |
| **CSS3** | Card layout, centered design, responsive styling |
| **JavaScript (Vanilla)** | `Date` object, age calculation logic, DOM update |
| **Vercel** | Deployment & hosting |

---

## 💡 Key Concepts Demonstrated

- **JavaScript `Date` Object** — Working with `getFullYear()`, `getMonth()`, `getDate()`
- **Date Arithmetic** — Correctly handling month/day borrowing during subtraction
- **DOM Manipulation** — Reading input value and updating result display
- **Input Validation** — Handling empty or invalid date selections
- **`onclick` Event** — Triggering function directly from HTML button attribute

---

## 🚀 Getting Started

### Run Locally

1. **Clone the repository**
   ```bash
   git clone https://github.com/Daniish-Qureshi/Person-Age-Calculator.git
   ```

2. **Navigate to the project folder**
   ```bash
   cd Person-Age-Calculator
   ```

3. **Open in browser**
   ```
   Open index.html directly in your browser
   — or use Live Server (VS Code extension)
   ```

> ✅ No API keys, no npm, no setup — just open and calculate!

---

## 📱 Responsive Design

| Screen | Behavior |
|--------|----------|
| **Mobile** | Full-width centered card, large date picker |
| **Tablet** | Comfortable card width with padding |
| **Desktop** | Centered calculator card with clean spacing |

---

## 👨‍💻 Author

**Danish Qureshi**  
BCA Final Year Student | Full Stack Developer  
📍 Dadri, Uttar Pradesh, India  
🔗 [GitHub — @Daniish-Qureshi](https://github.com/Daniish-Qureshi)  
🌐 [Portfolio](https://danish-qureshi-6ew5.vercel.app)

---

## 📄 License

This project is open source and free to use for **educational & portfolio purposes**.

---

⭐ If you found this useful, give it a **star** on GitHub!
