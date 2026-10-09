# Software Basics

## 🔢 Data Representation
### 🧠 What is it?
Computers only understand 1s and 0s (binary). Data representation is how computers convert our real-world data (numbers, images, text) into binary format and back.

### 📌 Key Concepts
- **Binary (Base-2):** Uses only 0 and 1. The language of computers.
- **Hexadecimal (Base-16):** Uses 0-9 and A-F. A shorter way to represent binary. Often used in memory addresses and color codes.
- **Bits and Bytes:** 8 bits = 1 byte.
- **RGB & Hex Colors:** How computers represent colors (e.g., #FFFFFF is white).

### 🎯 Pentester Perspective
- **Hex is Gold:** Reading Hex is crucial for reverse engineering and exploit development. You will see it in file headers, shellcode (`\x90\x90`), and network packets.
- **Analyzing Files:** Using tools like `xxd` or `hexdump` to view the raw binary of a file helps identify its true type (magic bytes) and hidden data.

---

## 🔤 Data Encoding
### 🧠 What is it?
Encoding is the process of converting data into a specific format for efficient transmission or storage. It is NOT encryption; it's just a different representation.

### 📌 Key Concepts
- **ASCII:** The oldest character encoding standard. Represents English characters using 7 bits.
- **Unicode:** A universal standard that supports characters from all languages.
- **UTF-8:** The most common encoding on the web. It is backward-compatible with ASCII.
- **Base64:** A binary-to-text encoding scheme. Often used to transmit data over media designed to handle textual data.

### 🎯 Pentester Perspective
- **Obfuscation:** Attackers use Base64 to hide malicious payloads in scripts, URLs, or web requests to bypass basic filters.
- **Web Attacks:** URL encoding (e.g., `%20` for space) is used in HTTP requests, and bypassing web application firewalls (WAF) often involves encoding payloads.
- **Encoding != Encryption:** Never confuse the two. Encoding is easily reversible.

---

## 🐍 Python: Simple Demo
### 🧠 What is it?
Python is a high-level, interpreted programming language known for its readability and simplicity.

### 📌 Key Concepts
- **Print:** `print("Hello, World!")` outputs text to the console.
- **Variables:** Containers for storing data values.
- **Data Types:** Strings, Integers, Floats, Booleans.
- **Interpreted:** Python code is executed line by line, making it great for scripting.

### 🎯 Pentester Perspective
- **The Pentester's Swiss Army Knife:** Python is the #1 language for writing custom hacking tools, exploit scripts, and automation.
- **Tools Built in Python:** Many popular tools (like Sqlmap, Impacket, and parts of Metasploit) are written in Python.

---

## 📜 JavaScript: Simple Demo
### 🧠 What is it?
JavaScript (JS) is the programming language of the web. It runs in the browser and makes websites interactive.

### 📌 Key Concepts
- **Client-Side:** Runs directly in the user's browser.
- **Console.log:** `console.log("Hello!")` prints output to the browser's developer console.
- **DOM (Document Object Model):** JS can manipulate HTML and CSS on the fly.

### 🎯 Pentester Perspective
- **XSS (Cross-Site Scripting):** This is the biggest web vulnerability involving JavaScript. Attackers inject malicious JS into a website, which executes in the victim's browser.
- **Bypassing Filters:** Understanding JS helps in crafting payloads that bypass web application security filters.

---

## 🗄️ Database SQL Basics
### 🧠 What is it?
A database is an organized collection of data. SQL (Structured Query Language) is the standard language used to communicate with relational databases.

### 📌 Key Concepts
- **Tables, Rows, and Columns:** How data is structured.
- **SELECT:** Retrieve data from a database.
- **WHERE:** Filter the data.
- **INSERT, UPDATE, DELETE:** Modify the data.
- **Example:** `SELECT * FROM users WHERE username = 'admin';`

### 🎯 Pentester Perspective
- **SQL Injection (SQLi):** This is one of the most critical web vulnerabilities (OWASP Top 10). If you don't understand basic SQL, you cannot exploit SQLi.
- **Data Breaches:** SQLi allows attackers to dump the entire database, steal credentials, and sometimes even execute system commands on the server.

---

## 📌 Module Key Takeaway
"Data is just 1s and 0s until we give it meaning through representation and encoding. Understanding how software (Python, JS) and databases (SQL) process this data is the foundation of modern cybersecurity."
