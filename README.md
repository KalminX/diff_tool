# 📝 Text Comparison Tool (Flask App)

A simple yet powerful web application that compares two text files and displays the differences in a **side-by-side view**, similar to **Microsoft Word's Compare feature**.

Built with **Flask**, styled with custom CSS, and deployed using **Gunicorn & Docker**.

---

## 🚀 Features

✅ Upload & compare two `.txt` files
✅ Side-by-side diff visualization (color-highlighted changes)
✅ Addition, deletion, and modification detection
✅ Clean, responsive, and professional UI
✅ Dockerized for easy deployment
✅ Gunicorn production-ready server

---

## 📸 Demo Screenshot

![Demo Screenshot](https://via.placeholder.com/900x400?text=Comparison+Tool+Demo+Screenshot)

---

## 🏗️ Project Structure

```
diff_tool/
├── app.py                # Flask application code
├── requirements.txt      # Python dependencies
├── Dockerfile            # Docker build instructions
├── templates/
│   └── result.html       # HTML template for result view
|   └── index.html
└── static/
    └── style.css         # Custom styles for comparison view
```

---

## 🐳 Quickstart with Docker

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/kalminx/diff_tool.git
cd text-diff-tool
```

### 2️⃣ Build Docker Image

```bash
docker build -t text-diff-app .
```

### 3️⃣ Run the App

```bash
docker run -p 5000:5000 text-diff-app
```

### 4️⃣ Open in Browser

```
http://localhost:5000/
```

---

## 🖼️ Usage

1. Open the app in your browser.
2. Upload **two text files** you wish to compare.
3. View the **highlighted differences** side-by-side.
4. Supports minor and major text changes.

---

## 📦 Tech Stack

* **Python 3.11**
* **Flask 2.2.x**
* **Gunicorn 21.x**
* **Docker (Slim Python Image)**
* **HTML & CSS (Custom diff styling)**

---

## 🛠️ Development Setup (Without Docker)

```bash
# Create virtual environment
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run the app
gunicorn --bind 0.0.0.0:5000 app:app
```

Visit: `http://localhost:5000/`

---

## ✨ Example of Diff View

| File 1                   | File 2                       |
| ------------------------ | ---------------------------- |
| This is an **old** line. | This is an **updated** line. |
| Another unchanged line.  | Another unchanged line.      |

* **Additions** are green ✅
* **Deletions** are red ❌
* **Changes** are yellow ⚠️

---

## 📄 License

This project is licensed under the MIT License.

---

## 🙌 Acknowledgements

* Python Standard Library: `difflib.HtmlDiff`
* Flask Documentation
* Microsoft Word Compare (for UI inspiration)

---

## 🔗 Author & Links

Made with ❤️ by [Kalmin](https://github.com/kalminx)

---

## ✅ TODO (Future Improvements)

* Inline word-level diff (like MS Word's inline mode)
* Markdown & DOCX file comparison support
* Drag & Drop file upload
* Dark mode UI

---

## ⭐ Give it a Star!

If you like this project, please give it a ⭐ on GitHub.
Helps visibility & motivation!
