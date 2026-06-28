# ✍️ WriteBox

A lightweight, file-based writing application built with **Node.js**, **Express.js**, **EJS**, and **Tailwind CSS**. WriteBox lets users create and read plain text files directly through a clean web interface, using Node's built-in `fs` (File System) module — no database required.

---

## Features

- **Create text files** — Submit content through a web form and persist it as a `.txt` file on the server
- **Read saved files** — View the content of previously created files through the browser
- **Server-side file I/O** — All file operations are handled using Node.js's native `fs` module
- **Dynamic HTML rendering** — Pages are rendered server-side using EJS templates
- **Responsive UI** — Styled with Tailwind CSS for a clean, utility-first interface
- **Static asset serving** — Custom CSS served from the `public/stylesheets/` directory via Express's static middleware

---

## Tech Stack

| Layer | Technology |
|---|---|
| Runtime | Node.js |
| Web Framework | Express.js |
| Templating Engine | EJS (Embedded JavaScript) |
| Styling | Tailwind CSS |
| File Storage | Node.js `fs` module (filesystem) |
| Package Manager | npm |

---

## Project Structure

```
WriteBox/
├── files/                  # Directory where user-created text files are stored
├── public/
│   └── stylesheets/        # Compiled/custom CSS files served as static assets
├── views/                  # EJS template files for server-rendered pages
├── index.js                # Main Express application entry point (routes & fs logic)
├── package.json            # Project metadata and dependencies
└── package-lock.json       # Locked dependency tree
```

> **Note:** `node_modules/` is present in the repository. It is recommended to add it to `.gitignore` in future.

---

## Installation

### Prerequisites

- [Node.js](https://nodejs.org/) (v14 or later recommended)
- npm (comes bundled with Node.js)

### Steps

```bash
# 1. Clone the repository
git clone https://github.com/Manasviii28/WriteBox.git

# 2. Navigate into the project directory
cd WriteBox

# 3. Install dependencies
npm install
```

---

## Environment Variables

WriteBox does not require any external environment variables in its current implementation. All configuration (such as the port number and file storage path) is handled directly inside `index.js`.

If you wish to customize the port, you can modify the relevant line in `index.js`:

```js
// Example: change the port
app.listen(3000);
```

---

## Usage

```bash
# Start the server
node index.js
```

Then open your browser and visit:

```
http://localhost:3000
```

From the web interface you can:
1. **Write** content and submit it to save it as a file on the server
2. **Read** the saved file content displayed back in the browser

---

## Screenshots

![Home Page](screenshots/home.png)

![Create File](screenshots/create.png)

![Read File](screenshots/read.png)

---

## Learning Outcomes

This project demonstrates practical understanding of several core web development concepts:

**Backend**
- Setting up an Express.js server and defining GET/POST routes
- Using Node.js's native `fs` module to write and read files from the server's filesystem
- Parsing form data submitted from the client using Express's body-parser middleware
- Serving static assets (CSS) with `express.static`

**Frontend / Templating**
- Building server-rendered pages using the EJS templating engine
- Passing dynamic data from Express route handlers into EJS views
- Structuring a multi-view application with reusable templates

**Styling**
- Applying utility-first CSS with Tailwind CSS in a Node.js/Express project

---

## Future Improvements

- Add a `.gitignore` file to exclude `node_modules/` from version control
- Implement a file listing page to browse all previously created files
- Add the ability to edit or delete existing files
- Introduce input validation to prevent empty or malformed file submissions
- Add flash messages for success/error feedback after form submission
- Support custom filenames provided by the user at creation time
- Deploy to a cloud platform (e.g., Render, Railway, or Vercel via serverless adapter)

---

## Author

**Manasvi**
GitHub: [@Manasviii28](https://github.com/Manasviii28)
