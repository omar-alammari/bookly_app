# 📚 Bookly App

Bookly App is a Flutter application for displaying and exploring books using the Google Books API.  
It allows users to browse books, view details, open books in the browser, and share them with others.  
The application is built using modern architectural practices and technologies to ensure scalability, maintainability, and performance.

## 🌟 Features

- **Splash Screen:** Provides a smooth user experience on startup.
- **Home Screen:** Displays a list of books fetched from the Google Books API.
- **Book Details:** View detailed information about each book upon clicking, along with similar books.
- **Similar Books:** Suggestions for similar books based on the selected book.
- **Open Book:** Open the book directly in the browser (if available).
- **Share Book:** Share book details with others.
- **Pagination:** Incremental loading of books for better performance.
- **Caching:** Uses Hive for local storage to reduce API requests.
- **Attractive UI:** Clean and intuitive user interface.

## 🚀 Technologies Used

- **Flutter:** Google's UI toolkit for building natively compiled apps.
- **Clean Architecture:** For separation of concerns and testability.
- **MVVM (Model-View-ViewModel):** To organize and manage UI logic.
- **Cubit (Bloc):** For efficient state management.
- **Get_it:** For dependency injection.
- **Hive:** A lightweight and fast NoSQL database for caching.
- **Google Books API:** The main data source.
- **Dio:** Powerful HTTP client for network requests.
- **URL Launcher:** For opening external URLs.
- **Share Plus:** For content sharing.

## 📂 Project Structure

```
lib/
├── core/                  # Utilities and helpers (constants, errors, etc.)
│   ├── errors/
│   └── utils/
├── features/              # Application features/modules
│   ├── home/
│   │   ├── data/
│   │   │   ├── datasources/   # Remote & local data sources
│   │   │   ├── models/        # Data models from API
│   │   │   └── repos/         # Repository implementations
│   │   ├── domain/
│   │   │   ├── entities/      # Clean entities
│   │   │   ├── repos/         # Repository interfaces
│   │   │   └── use_cases/     # Business logic
│   │   └── presentation/
│   │       ├── manager/       # Cubits (state management)
│   │       ├── views/         # UI screens
│   │       └── widgets/       # Reusable UI components
│   └── search/                # Search feature (example)
├── main.dart                 # Application entry point
```


## 🖼️ Screenshots

> Add screenshots here to showcase the app. Example:  
> ![Bookly App Screenshot](path/to/screenshot.png)

## ⚙️ Installation & Setup

To run this project locally:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/omar-alammari/bookly_app.git
   cd bookly_app
   ```

2. **Install dependencies:**
   ```bash
   flutter pub get
   ```

3. **Run the app:**
   ```bash
   flutter run
   ```

## 👨‍💻 Usage

1. **Browse Books:** View books on the main screen.
2. **Tap a Book:** See full book details and similar suggestions.
3. **Open Book:** If available, opens in the browser.
4. **Share Book:** Share with friends or others.

## 🤝 Contributing

Contributions are welcome!

1. **Fork the repo**
2. **Create a branch:**  
   ```bash
   git checkout -b feature/YourFeature
   ```
3. **Make changes**
4. **Commit:**  
   ```bash
   git commit -m "feat: add new feature"
   ```
5. **Push:**  
   ```bash
   git push origin feature/YourFeature
   ```
6. **Open a Pull Request**

## 📄 License

This project is licensed under the MIT License.  
See the [LICENSE](LICENSE) file for details.
