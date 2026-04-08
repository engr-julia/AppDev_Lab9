# 🌌 Cosmic Gallery

A high-performance, visually immersive web application built with **PHP**, **MySQL**, and **AJAX**. This gallery features a dynamic starry background with interactive elements and a real-time "live search" system to filter celestial bodies instantly.

## 🚀 Key Features

* **Live Search:** Filter stars by name instantly without page refreshes using jQuery and AJAX.
* **High-Visibility UI:** Optimized color contrast and text-shadows ensure readability against the dark space theme, even in hover mode.
* **Cosmic Animations:** * **Moving Pictures:** Images scale and rotate smoothly when hovering over table rows.
    * **Dynamic Background:** An HTML5 Canvas script generating twinkling stars and shooting stars at 60FPS.
* **Full CRUD Functionality:** Support for Creating, Reading, Updating, and Deleting celestial entries.
* **Responsive Design:** Built with Bootstrap for a clean layout across different screen sizes.

---

## 📂 File Structure

| File | Role |
| :--- | :--- |
| **`db.php`** | Configuration for the PDO database connection. Included in all functional scripts. |
| **`index.php`** | The main gallery interface. Contains the search bar, the star table, and the animation logic. |
| **`search_ajax.php`** | The background "worker" script. Processes search queries and returns HTML table rows. |
| **`selected.php`** | Detailed view page for a specific star. |
| **`create.php`** | Form for adding new stars with image upload capabilities. |
| **`edit.php`** | Interface for modifying existing star data and updating images. |
| **`delete.php`** | A background script that handles record removal and redirects to the gallery. |
| **`/uploads`** | Directory where all celestial images are stored. |

---

## 🛠️ Installation & Setup

### 1. Database Configuration
Create a MySQL database (e.g., `if0_41604144_cosmic`) and run the following SQL command to create the table:

```sql
CREATE TABLE characters (
    id INT AUTO_INCREMENT PRIMARY KEY,
    title VARCHAR(255) NOT NULL,
    author VARCHAR(255) NOT NULL,
    descriptions TEXT NOT NULL,
    image VARCHAR(255)
);
### 2. Connect to the Server
Edit db.php with your database credentials:

Host: sql100.infinityfree.com

User: if0_41604144

Pass: *********

### 3. Folder Permissions
Ensure the uploads/ folder is created and has write permissions (755 or 777) so that the server can save uploaded images.

🧪 Technical Overview
AJAX Live Search Logic
When a user types in the search input on index.php, a jQuery function captures the input and sends it to search_ajax.php via a GET request. The server-side script performs a LIKE query:

SQL
SELECT * FROM characters WHERE title LIKE '%search_term%'
The resulting rows are sent back as raw HTML and injected directly into the <tbody> of the table without a page reload.

Hover Visibility Enhancement
To prevent text from disappearing against the dark background, specific CSS overrides are applied:

Background: rgba(110, 68, 255, 0.45) provides a distinct purple highlight.

Text Glow: text-shadow: 0 0 8px rgba(255, 255, 255, 0.6) ensures the white text remains sharp and visible.

## 📜 Credits & License
Created as a customized Cosmic Gallery project. Designed for performance on InfinityFree hosting environments.

May your code shine as bright as the stars! 🌠


---

### How to use this:
1.  Open your code editor (like Notepad++, VS Code, or the InfinityFree file manager).
2.  Create a new file called **`README.md`**.
3.  **Copy and Paste** everything inside the grey block above.
4.  Save the file. It will now serve as the official documentation for your project!
