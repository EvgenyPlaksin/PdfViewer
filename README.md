# PDF Viewer

PDF Viewer is an Android application built using Jetpack Compose that allows users to view and search within PDF documents. The app leverages the `PdfRenderer` class to convert PDF pages into bitmaps, which are then displayed using Compose's `LazyColumn`. This project is intended to demonstrate the integration of Android's PDF rendering capabilities with modern Compose UI.

## Features

- **PDF Selection**: Users can choose a PDF document from their device storage.
- **PDF Rendering**: The app renders each page of the selected PDF as a bitmap and displays them vertically.
- **Search Functionality**: Users can search for text within the PDF. The search results are highlighted on the corresponding pages. (Note: The search feature is available only on devices running Android 15 (API level 34) and above.)

## Prerequisites

- **Minimum SDK**: 24
- **Target SDK**: 35
- **Compile SDK**: 35

## Technologies Used

- **Jetpack Compose**: For building the user interface in a declarative way.
- **PdfRenderer**: To convert PDF pages into bitmaps.
- **Kotlin Coroutines**: For handling asynchronous tasks, such as PDF rendering and text search.
- **Coil**: For loading and displaying images in Compose.

## How It Works

1. **PDF Selection**: The user selects a PDF file using the `ActivityResultContracts.GetContent` contract.
2. **Rendering PDF**: Once a PDF is selected, the `PdfBitmapConverter` class uses `PdfRenderer` to convert each page into a `Bitmap`.
3. **Displaying PDF**: The rendered bitmaps are displayed using a `LazyColumn` in the `PdfViewerScreen` composable.
4. **Search Functionality**: If the device is running Android 15 or higher, the user can search for text within the PDF. The app will highlight the search results on the pages where the text is found.

## Limitations

- **Search Functionality**: The search feature is only available on devices running Android 15 (API level 34) or higher. This is due to the introduction of new search APIs in the PdfRenderer class that are not available on earlier versions of Android.

## Setup and Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/pdfviewer.git
    ```
2. Open the project in Android Studio.
3. Build and run the project on a device or emulator with a minimum API level of 24.

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.

## License

This project is licensed under the MIT License.
