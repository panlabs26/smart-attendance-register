# 📋 Smart Attendance Register
### KLS Gogte Institute of Technology · ISE Department · 2025–26

> A serverless, real-time digital attendance system for classroom and lab sessions.
> Hosted free on **GitHub Pages** · Powered by **Firebase Realtime Database** · Zero server cost.

---

## 🔗 Live URLs

| Role | URL |
|------|-----|
| 🎓 Student | `https://panlabs26.github.io/smart-attendance-register/` |
| 👩‍💻 Professor | `https://panlabs26.github.io/smart-attendance-register/?prof=1` |

---

## ✨ Features

### 🎓 Student Side
- Select Division A or B
- Enter USN — name previews instantly
- Enter 4-digit session token
- Submit — permanent success screen shown
- Blocks: wrong division / wrong token / invalid USN / duplicate / paused session

### 👩‍💻 Professor Side
- Password-protected dashboard (`?prof=1` → password: `1111`)
- Division, Date, Period Time (auto-filled)
- Open / Pause / Resume / Close session
- 5-minute countdown timer — auto-closes at zero
- Live Present / Absent / Total stats
- Flash card notification when student marks attendance
- Status badge — OPEN / PAUSED / CLOSED

### 📂 Professor Tools Panel (bottom-right corner)
**Tab 1 — Students.js Generator:**
- Drop college Excel → auto-detects Div A & B sheets
- Preview student list before download
- Download ready-to-use `students.js`

**Tab 2 — Course Config:**
- Set Institution, Department, Subject, Code, Professor Name, Year
- Saved to browser localStorage — survives reload
- Instantly reflects in header bar and Excel export

### 📥 Excel Export (KLS Format)
- All sessions as columns — P/A per student
- Rotated date+time headers (`dd.mm.yyyy` + `h.mmam/pm`)
- Color-coded P (green) / A (red)
- DAY TOTAL row, Total attended, Attendance %
- Frozen panes for easy scrolling
- Filename: `SAR_[code]_Div[X]_[date].xlsx`

---

## 🗂 File Structure

```
smart-attendance-register/
├── index.html      ← Full app — all logic, UI, Firebase, Excel export
├── students.js     ← Student list — Division A & B
├── style.css       ← Base dark theme
└── README.md
```

---

## 🛠 Tech Stack

| Layer | Technology |
|-------|-----------|
| Hosting | GitHub Pages (free) |
| Database | Firebase Realtime Database (free) |
| Frontend | Vanilla HTML + CSS + JavaScript |
| Fonts | Google Fonts — Sora + Space Mono |
| Excel | xlsx-js-style v1.2.0 via CDN |
| Firebase SDK | v10.12.0 via CDN (ES Module) |

---

## 🔐 Access

- Student URL — plain URL, share with class
- Professor URL — add `?prof=1`, password: `1111`
- Change password: edit `PROF_PASS` constant in `index.html`

---

## 🚀 Deploy for a New Subject (Your Colleague's Guide)

1. **Firebase** — Create project → Realtime Database → test mode rules → copy `firebaseConfig`
2. **index.html** — Replace `firebaseConfig` block with your own
3. **GitHub** — New public repo → upload 3 files → enable Pages (Settings → Pages → main/root)
4. **Config** — Open `?prof=1` → 📂 → ⚙️ Course Config → fill your subject details → Save
5. **Students** — 📂 → Students.js tab → drop college Excel → Download → upload to repo

---

## 👨‍🏫 Developed by

**Prof. Pandurang Upparamani**
Department of Information Science & Engineering
KLS Gogte Institute of Technology, Belagavi
