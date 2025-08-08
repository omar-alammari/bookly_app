# 📚 Bookly App

Bookly App is a Flutter application for displaying and exploring books using the Google Books API.  
It allows users to browse books, view details, open books in the browser, and share them with others.  
The application is built using modern architectural practices and technologies to ensure scalability, maintainability, and performance.

---

## 📱 Screenshots

| Home Screen | Home Screen |
|:---:|:---:|
| ![Home Screen](assets/screenshots/1-home.png) | ![Details Book Screen](assets/screenshots/2-details.png) |

---

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

---

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
├── assets/
│   ├── fonts/
│   │   └── GT Sectra Fine Regular.ttf
│   ├── images/
│   │   ├── Logo.png
│   │   └── test_image.png
│   └── screenshots/
│       ├── 1-home.png
│       └── 2-details.png
├── lib/
│   ├── Features/
│   │   ├── Splash/
│   │   │   └── presentation/
│   │   │       └── views/
│   │   │           ├── splash_view.dart
│   │   │           └── widgets/
│   │   │               ├── sliding_text.dart
│   │   │               └── splash_view_body.dart
│   │   ├── home/
│   │   │   ├── data/
│   │   │   │   ├── data_sources/
│   │   │   │   │   ├── home_local_data_source.dart
│   │   │   │   │   └── home_remote_data_source.dart
│   │   │   │   ├── models/
│   │   │   │   │   └── book_model/
│   │   │   │   │       ├── access_info.dart
│   │   │   │   │       ├── book_model.dart
│   │   │   │   │       ├── epub.dart
│   │   │   │   │       ├── image_links.dart
│   │   │   │   │       ├── industry_identifier.dart
│   │   │   │   │       ├── panelization_summary.dart
│   │   │   │   │       ├── pdf.dart
│   │   │   │   │       ├── reading_modes.dart
│   │   │   │   │       ├── sale_info.dart
│   │   │   │   │       ├── search_info.dart
│   │   │   │   │       └── volume_info.dart
│   │   │   │   └── repos/
│   │   │   │       └── home_repo_impl.dart
│   │   │   ├── domain/
│   │   │   │   ├── entities/
│   │   │   │   │   ├── book_entity.dart
│   │   │   │   │   └── book_entity.g.dart
│   │   │   │   ├── repos/
│   │   │   │   │   └── home_repo.dart
│   │   │   │   └── use_cases/
│   │   │   │       ├── fetch_featured_books_use_case.dart
│   │   │   │       └── fetch_newest_books_use_case.dart
│   │   │   └── presentation/
│   │   │       ├── manger/
│   │   │       │   ├── featured_books_cubit/
│   │   │       │   │   ├── featured_books_cubit.dart
│   │   │       │   │   └── featured_books_state.dart
│   │   │       │   └── newset_books_cubit/
│   │   │       │       ├── newest_books_cubit.dart
│   │   │       │       └── newest_books_state.dart
│   │   │       └── views/
│   │   │           ├── book_details_view.dart
│   │   │           ├── home_view.dart
│   │   │           └── widgets/
│   │   │               ├── best_seller_list_view.dart
│   │   │               ├── best_seller_list_view_item.dart
│   │   │               ├── book_details_view_body.dart
│   │   │               ├── book_rating.dart
│   │   │               ├── books_action.dart
│   │   │               ├── books_details_sectioni.dart
│   │   │               ├── custom_app_bar.dart
│   │   │               ├── custom_book_details_app_bar.dart
│   │   │               ├── custom_book_image_loading_indicator.dart
│   │   │               ├── custom_book_item.dart
│   │   │               ├── featured_books_list_view_bloc_builder.dart
│   │   │               ├── featured_books_list_view_loading_indicator.dart
│   │   │               ├── featured_list_view.dart
│   │   │               ├── home_view_body.dart
│   │   │               ├── similar_books_list_view.dart
│   │   │               └── similar_books_section.dart
│   │   └── search/
│   │       └── presentation/
│   │           └── views/
│   │               ├── search_view.dart
│   │               └── widgets/
│   │                   ├── custom_search_text_field.dart
│   │                   └── search_view_body.dart
│   ├── constants.dart
│   ├── core/
│   │   ├── errors/
│   │   │   └── failure.dart
│   │   ├── use_cases/
│   │   │   └── use_case.dart
│   │   ├── utils/
│   │   │   ├── api_service.dart
│   │   │   ├── app_router.dart
│   │   │   ├── assets.dart
│   │   │   ├── functions/
│   │   │   │   ├── build_error_snack_bar.dart
│   │   │   │   ├── save_books.dart
│   │   │   │   └── setup_service_locator.dart
│   │   │   ├── simple_bloc_observer.dart
│   │   │   └── styles.dart
│   │   └── widgets/
│   │       ├── custom_button.dart
│   │       └── custom_fading_widget.dart
│   └── main.dart
└── 
```

---

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
