# 📝 File Comparison Tool

🔗 **Live Demo:** [diff-tool](https://diff-tool.up.railway.app/)

A robust web application that compares two files (`.txt`, `.docx`, or `.pdf`) and displays their differences side-by-side, inspired by tools like Microsoft Word's *Compare* feature.

The app performs MIME type validation to ensure only valid files are processed, and provides user-friendly error messages for invalid uploads. Built with Flask, styled with custom CSS, and deployed using **Gunicorn** & **Docker** for scalability and ease of use.

---

## 🚀 Features

* ✅ Upload and compare `.txt`, `.docx`, and `.pdf` files
* ✅ Side-by-side diff visualization with color-highlighted changes
* ✅ Detects additions, deletions, and modifications
* ✅ MIME type validation using **libmagic** to prevent invalid uploads
* ✅ Flash messages for user feedback on invalid files
* ✅ Export comparison results as `.txt`, `.docx`, or `.pdf`
* ✅ Clean, responsive, and modern UI with custom styling
* ✅ Dockerized for seamless deployment
* ✅ Production-ready with **Gunicorn**

---

## 📸 Demo Screenshot

*(Add an actual screenshot image here)*

---

## 🏗️ Project Structure

```
diff_tool/
├── app.py                # Flask application code
├── requirements.txt      # Python dependencies
├── Dockerfile            # Docker build instructions
├── templates/
│   ├── index.html        # File upload interface
│   └── result.html       # Comparison result view
└── static/
    └── css/
        └── style.css     # Custom styles for UI and diff table
```

---

## 🐳 Quickstart with Docker

1. **Clone the Repository**

   ```bash
   git clone https://github.com/kalminx/diff_tool.git
   cd diff_tool
   ```

2. **Build Docker Image**

   ```bash
   docker build -t file-diff-app .
   ```

3. **Run the App**

   ```bash
   docker run -p 5000:5000 file-diff-app
   ```

4. **Open in Browser**

   ```
   http://localhost:5000/
   ```

---

## 🖼️ Usage Guide

1. Open the app in your browser.
2. Upload two files (`.txt`, `.docx`, or `.pdf`) to compare.
3. View the differences in a side-by-side comparison table.
4. Export the comparison results as `.txt`, `.docx`, or `.pdf`.
5. If an invalid file is uploaded, a flash message will display an error.

---

## 📦 Tech Stack

* **Python 3.11**
* **Flask 3.0.3**
* **Gunicorn 23.0.0**
* **Docker (Python 3.11-slim image)**
* **python-docx 1.1.2** (DOCX processing)
* **PyMuPDF 1.24.9** (PDF processing)
* **reportlab 4.2.2** (PDF export)
* **python-magic 0.4.27** (MIME type validation)
* **HTML & CSS** (custom diff styling with responsive design)

---

## 🛠️ Development Setup (Without Docker)

1. **Install system dependencies** (for libmagic)

   ```bash
   sudo apt-get update
   sudo apt-get install -y libmagic1
   ```

2. **Create and activate a virtual environment**

   ```bash
   python -m venv venv
   source venv/bin/activate  # Windows: venv\Scripts\activate
   ```

3. **Install Python dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Run the app**

   ```bash
   gunicorn --bind 0.0.0.0:5000 app:app
   ```

Visit: [http://localhost:5000/](http://localhost:5000/)

---

## ✨ Example Diff View

| File 1                   | File 2                       |
| ------------------------ | ---------------------------- |
| This is an **old** line. | This is an **updated** line. |
| Another unchanged line.  | Another unchanged line.      |

* ✅ **Additions** are highlighted in green
* ❌ **Deletions** are highlighted in red

---

## 📄 License

This project is licensed under the **MIT License**.

---

## 🙌 Acknowledgements

* Python Standard Library: **difflib.HtmlDiff** for comparison logic
* Flask Documentation for web framework guidance
* **libmagic** & **python-magic** for MIME type validation
* UI inspiration from Microsoft Word Compare & GitHub Diff views

---

## 🔗 Author & Links

Made with ❤️ by **Kalmin**

* **Deployed App:** [https://diff-tool.up.railway.app/](https://diff-tool.up.railway.app/)
* **GitHub Repository:** *(Add GitHub repo link here)*

---

## ✅ TODO (Future Improvements)

* Support inline word-level diff highlighting (like MS Word's inline mode)
* Add drag-and-drop file upload functionality
* Implement dark mode for the UI
* Support additional file formats (`.rtf`, `.md`, etc.)
* Add file size validation and progress indicators for large files
* Store comparison results in a database for history

---

## ⭐ Support the Project

If you like this project, please consider giving it a ⭐ on GitHub.
It helps with visibility and keeps the motivation high!
