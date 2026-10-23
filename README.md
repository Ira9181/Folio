# 📄 Folio

**Folio – The Offline Document Studio.**

Folio is an offline document scanner and document manager built with Flutter.
Scan pages with your camera or gallery, crop and enhance them, add signatures,
organize them into folders, and export everything as high-quality PDFs — all
data stays securely on-device (SQLite), no internet required.

---

## ✨ Features

- 📸 **Scan documents** — from the camera or pick multiple images from the gallery
- ✂️ **Crop pages** — interactive cropping via `image_cropper`
- 🎨 **Apply filters** — Original, Magic Color, Black & White, Greyscale
  (color-matrix filters defined in `lib/core/color_filters.dart`)
- ✍️ **Add digital signatures** — hand-drawn signature pad (`signature`)
- 🧠 **Smart naming** — on-device Google ML Kit text recognition auto-suggests
  document names (`Invoice`, `Amazon_Invoice`, `Passport_Scan`, `ID_Card`, …)
- 📂 **Organize into folders** — create folders, browse documents by folder
- 🔄 **Reorder, add & delete pages** — per-document page management
- 📑 **Generate & share PDFs** — export as PDF and share via the share sheet
- 💾 **Offline storage** — SQLite (`sqflite`) with local image files
- 🌙 **Material 3 UI** — light & dark mode, Poppins typography

---

## 🛠 Tech Stack

| Layer         | Technology                                              |
| ------------- | ------------------------------------------------------- |
| Framework     | Flutter (Dart)                                          |
| State mgmt    | Flutter BLoC + Equatable                                |
| Database      | SQLite via `sqflite`                                    |
| OCR / naming  | Google ML Kit Text Recognition (on-device)              |
| Media         | `image_picker`, `image_cropper`, `file_picker`          |
| PDF           | `pdf`, `open_filex`, `share_plus`                       |
| Signature     | `signature`                                             |
| UI            | Material 3, `google_fonts`, `intl`                      |

---

## 📁 Project Structure

```
lib/
├── blocs/
│   ├── dashboard/    # dashboard state (folders, recent docs)
│   └── scanner/      # scanning flow state (pick → review → save)
├── core/
│   ├── color_filters.dart     # color-matrix filters (Original/Magic/B&W/Grey)
│   └── database_helper.dart   # SQLite setup + CRUD
├── models/
│   ├── document_model.dart
│   ├── folder_model.dart
│   └── page_model.dart
├── repositories/
│   └── document_repository.dart
├── services/
│   ├── scanner_service.dart   # image picking + ML Kit smart naming
│   └── pdf_service.dart       # PDF generation & export
├── ui/
│   ├── screens/       # dashboard, scanner, studio, document detail, folder view
│   └── widgets/       # document & folder list tiles
└── main.dart          # app entry, DI wiring, theming
```

---

## 🗄 Data Model

Three SQLite tables with foreign-key cascade deletes:

| Table       | Fields                                                    |
| ----------- | --------------------------------------------------------- |
| `folders`   | `id`, `name`, `createdAt`                                 |
| `documents` | `id`, `folderId`, `name`, `createdAt`                     |
| `pages`     | `id`, `documentId`, `imagePath`, `pageOrder`, `metadata`  |

A default **"Uncategorized"** folder is created on first launch.

---

## 🚀 Getting Started

### Prerequisites

- Flutter SDK (Dart `^3.11.5`)
- Android Studio / VS Code
- Android emulator or a physical device

### Run

```bash
git clone <https://github.com/Ira9181/Folio.git>
cd Folio

flutter pub get
flutter run
```

---

## 🧭 App Flow

1. **Dashboard** — recent documents + folders overview
2. **Scan** — pick images (camera/gallery) → ML Kit suggests a name
3. **Studio** — per-page crop, filter, and signature editing
4. **Review** — reorder / add / delete pages
5. **Export** — generate PDF and share / open

---

## 🔮 Future Improvements

- Cloud synchronization
- OCR-based document search
- Password-protected PDFs
- Document sharing via QR
- Multi-language OCR support

---

## 👩‍💻 Author

**Ira Ratan Vatsyayan** · [GitHub](https://github.com/Ira9181)
