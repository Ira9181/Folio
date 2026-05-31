# Folio – The Offline Document Studio 📄✨

**Folio** is a powerful, privacy-first offline document scanner and editor built with Flutter. It allows users to scan documents, organize them into folders, apply professional filters, add digital signatures, and export them as high-quality PDFs—all without ever needing an internet connection.

---

## 🚀 Key Features

- **🛡️ 100% Offline & Private:** No cloud uploads. Your documents stay on your device.
- **🔍 Smart Naming:** Uses **Google ML Kit** to recognize text in your scans and suggest relevant document names (e.g., "Amazon Invoice").
- **🎨 Folio Studio:**
  - **Professional Filters:** Magic Color, B&W, and Greyscale matrices.
  - **Digital Signature:** Hand-draw your signature directly on any page.
  - **Precise Cropping:** Adjust edges for a perfect scan.
- **📂 Smart Organization:** Categorize your scans into custom folders.
- **📑 Document Management:** Easily reorder pages, add more scans to existing documents, or delete unwanted pages.
- **📄 PDF Export & Share:** Generate high-quality PDFs and share them via your favorite apps.
- **🌓 Modern UI:** Sleek Material 3 design with support for Light and Dark modes.

---

## 🛠️ Tech Stack

- **Framework:** [Flutter](https://flutter.dev/)
- **State Management:** [Flutter BLoC](https://pub.dev/packages/flutter_bloc) (with Equatable)
- **Database:** [SQFlite](https://pub.dev/packages/sqflite) (Local SQLite storage)
- **AI/ML:** [Google ML Kit Text Recognition](https://pub.dev/packages/google_mlkit_text_recognition)
- **Imaging:** [Image Picker](https://pub.dev/packages/image_picker), [Image Cropper](https://pub.dev/packages/image_cropper)
- **PDF Engine:** [PDF](https://pub.dev/packages/pdf)
- **UI:** [Google Fonts (Poppins)](https://pub.dev/packages/google_fonts), [Signature](https://pub.dev/packages/signature)

---

## 📁 Project Structure

```text
lib/
├── blocs/          # Business logic for Dashboard and Scanner
├── core/           # Database helpers and constant color filters
├── models/         # Data models for Folders, Documents, and Pages
├── repositories/   # Data abstraction layer (Repository Pattern)
├── services/       # External services (ML Kit, PDF Gen, Image Picking)
├── ui/
│   ├── screens/    # Full-screen widgets (Dashboard, Studio, Scanner, etc.)
│   └── widgets/    # Reusable UI components (ListTiles, Grids)
└── main.dart       # App entry point and dependency injection
```

---

## ⚙️ Installation & Setup

1. **Prerequisites:**
   - Flutter SDK (v3.11.5 or higher recommended)
   - Android Studio / VS Code
   - A physical device or emulator

2. **Clone the repository:**
   ```bash
   git clone https://github.com/Ira9181/Folio.git
   cd Folio
   ```

3. **Install dependencies:**
   ```bash
   flutter pub get
   ```

4. **Run the app:**
   ```bash
   flutter run
   ```

---

## 📸 Screenshots

| Dashboard | Scanner | Studio |
| :---: | :---: | :---: |
| ![Dashboard Placeholder](https://via.placeholder.com/200x400?text=Dashboard) | ![Scanner Placeholder](https://via.placeholder.com/200x400?text=Scanner) | ![Studio Placeholder](https://via.placeholder.com/200x400?text=Studio) |

---

## 📜 License

Distributed under the MIT License. See `LICENSE` for more information.

---

**Developed with ❤️ by [Ira9181](https://github.com/Ira9181)**
