# Week 5 - Ethical Hacking & Exploiting Vulnerabilities

## 📌 Tasks
1. **Ethical Hacking Basics**
   - Used Kali Linux for penetration testing
   - Conducted reconnaissance on OWASP Juice Shop test web application

2. **SQL Injection (SQLi) & Exploitation**
   - Detected SQLi vulnerabilities using `sqlmap`
   - Example command:
     ```bash
     sqlmap -u "http://localhost:3000/rest/products?id=1" --batch --level=2 --risk=1 --dbs
     ```
   - Found injection in `id` parameter.

   ✅ **Fix:** Used prepared statements (`mysql2`) instead of string concatenation.

3. **Cross-Site Request Forgery (CSRF) Protection**
   - Implemented `csurf` middleware in Node.js
   - Tested CSRF with Burp Suite

---

## 📂 Project Structure
```
week5_sql_injection_project/
│── code/
│   ├── vulnerable.js   # vulnerable SQL code example
│   ├── fixed.js        # fixed SQL code with prepared statements
│── report/
│   ├── Week5_Report.md # detailed explanation + screenshots
│── screenshots/        # paste sqlmap screenshots here
│── README.md
```

---

## 📝 Instructions
1. Run **vulnerable.js**:
   ```bash
   node code/vulnerable.js
   ```
   Then test SQLi with SQLMap.

2. Run **fixed.js**:
   ```bash
   node code/fixed.js
   ```
   Re-test with SQLMap.  
   It should say **no injection found**.

3. Paste your screenshots inside `/screenshots/` folder.

---

## 🚀 Deliverables
- SQLMap output before & after fix (screenshots)
- Fixed code (`fixed.js`)
- Internship report (`Week5_Report.md`)
