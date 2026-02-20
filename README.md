Dicoding Books
📚 Project Description

Dicoding Books is a CRUD (Create, Read, Update, Delete) web application for managing book data connected to the Dicoding Books API. This application is built using JavaScript ES6+ with an asynchronous programming approach utilizing async/await and the Fetch API.
✨ Key Features

    📖 Display a list of books from the Dicoding API.

    ➕ Add new books with validation.

    ✏️ Update information for existing books.

    🗑️ Delete books from the list.

    🔄 Real-time updates without page reloads.

    🎨 Responsive design using Bootstrap 4.

🛠️ Technologies Used
Frontend

    HTML5 – Page structure.

    CSS3 with Bootstrap 4 – Styling and layout.

    JavaScript ES6+ – Application logic.

    Fetch API – Communication with the backend.

    Async/Await – Asynchronous operation handling.

Build Tools

    Webpack 5 – Module bundler.

    Babel – ES6+ to ES5 transpiler.

    Webpack Dev Server – Development server.

    HTML Webpack Plugin – HTML template processing.

---

📁 Project Structure
---
```
dicoding-books/

├── src/

│ ├── index.html # Main HTML template

│ ├── index.js # Application entry point

│ ├── scripts/

│ │ └── main.js # Main CRUD operations logic

│ └── styles/

│   └── main.css          # Custom styling

├── webpack.common.js   # Shared webpack configuration

├── webpack.dev.js      # Development configuration

├── webpack.prod.js     # Production configuration

├── package.json    # Dependencies and scripts

├── package-lock.json # Detailed notes on each dependency version

└── README.md # Project documentation
```

🚀 How to Run Installation Bash
--

npm install

Development Mode
Bash

npm run start-dev

The application will run at http://localhost:8080
Production Build
Bash

npm run build

The build output will be available in the dist/ folder.
🔧 API Endpoints
Method Endpoint Description
GET /list Get all books
POST /add Add a new book
PUT /edit/{id} Update a book
DELETE /delete/{id} Delete a book
Required Headers
JavaScript

{
'Content-Type': 'application/json',
'X-Auth-Token': '12345'
}


📋 Book Data Structure JavaScript
==
{
id: Number, // Unique Book ID
title: String, // Book Title
author: String // Author Name
}

💻 Primary JavaScript Functions

    getBook(): Fetches all book data from the API and renders it to the DOM.

    insertBook(book): Adds a new book to the system.

    updateBook(book): Updates existing book information.

    removeBook(bookId): Deletes a book based on its ID.

    renderAllBooks(books): Renders the book list into Bootstrap cards.

🎯 Usage Examples
Adding a New Book
JavaScript
---
const newBook = {
id: 101,
title: "JavaScript: The Good Parts",
author: "Douglas Crockford"
};
insertBook(newBook);

Updating a Book
JavaScript

const updatedBook = {
id: 101,
title: "JavaScript: The Definitive Guide",
author: "David Flanagan"
};
updateBook(updatedBook);

Deleting a Book
JavaScript

removeBook(101); // Deletes the book with ID 101

⚠️ Error Handling
---

The application handles various types of errors:

    Network errors – Disconnected internet connection.

    API errors – Invalid server response.

    CORS errors – Cross-origin restrictions.

    Validation errors – Invalid input data.

🧪 Testing

To test the API manually, use curl:
Bash

# Test GET

curl https://books-api.dicoding.dev/list

# Test POST

curl -X POST https://books-api.dicoding.dev/add \
 -H "Content-Type: application/json" \
 -H "X-Auth-Token: 12345" \
 -d '{"id":1,"title":"Test","author":"Author"}'

🔍 Debugging Tips
---

    Browser DevTools – Use the Network tab to monitor request/response.

    Console Logging – Add console.log() within async functions.

    Response Validation – Always check response.ok before parsing JSON.

    Error Messages – Use error.message for clearer error info.

📦 Dependencies Development
---
    webpack & webpack-cli – Module bundling.

    webpack-dev-server – Development server.

    babel-loader – JavaScript transpilation.

    html-webpack-plugin – HTML processing.

Production

    bootstrap – UI framework.

    regenerator-runtime – Async/await support.

🔄 Workflow

    User opens the application → getBook() is called.

    Book data is displayed in cards.

    User inputs new data → Client-side validation occurs.

    Data is sent to the API → Response is processed.

    DOM is updated without a page reload.

🎨 UI/UX Features

    Card-based layout for the book list.

    Real-time form validation.

    Feedback messages for every operation.

    Responsive grid system (Bootstrap).

    Consistent color scheme (Bootstrap Primary).

🚀 Optimization

    Code splitting with Webpack.

    ES6+ to ES5 transpilation for browser compatibility.

    Minification in the production build.

    Cache busting with hashed filenames.

📝 Development Notes

    Ensure a stable internet connection for API calls.

    Use async/await for a cleaner code flow.

    Implement error handling in every fetch request.

    Validate data before sending it to the API.

🤝 Contribution

    Fork the repository.

    Create a feature branch (git checkout -b feature/AmazingFeature).

    Commit your changes (git commit -m 'Add some AmazingFeature').

    Push to the branch (git push origin feature/AmazingFeature).

    Open a Pull Request.

📄 License

Distributed under the ISC License. See LICENSE for more information.
🙏 Acknowledgments

    Dicoding Indonesia – For providing the API and learning materials.

    Bootstrap – For the UI framework.

    Webpack – For the build tools.

🎯 Achievement Targets

    ✅ CRUD Operations – Full implementation.

    ✅ Async Programming – Using async/await.

    ✅ Error Handling – Comprehensive error management.

    ✅ Responsive Design – Mobile-friendly interface.

    ✅ Clean Code – Well-structured JavaScript.

    ✅ Build Optimization – Webpack configuration.
