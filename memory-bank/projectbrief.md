# Project Brief: ContextPack

## 1. Project Goal

To create a **client-side only** single-page web application (HTML, CSS, JavaScript) named **ContextPack** that allows users to upload a `.zip` archive or a folder. The application will read the archive's or folder's contents, concatenate the text content (and optionally Base64-encoded binary content) into a single formatted string, and display this string for easy copying into Large Language Model (LLM) prompts.

## 2. Core Requirements

*   **Input:** Accept either a `.zip` file via an HTML file input, or a folder via a separate input using the `webkitdirectory` attribute.
*   **Processing:** All decompression and content processing MUST occur in the user's browser using JavaScript. **No backend/server-side code.**
*   **Library:** Utilize the JSZip library for client-side ZIP handling, and the FileReader API for folder processing.
*   **Content Extraction:** Iterate through all files within the ZIP or the selected folder.
*   **File Type Handling:**
    *   Distinguish between text and binary files (using common file extensions as a primary guide).
    *   Include text files as UTF-8 strings.
    *   Provide a checkbox (`id="includeBinary"`) to optionally include binary files.
    *   If included, encode binary files as Base64 strings.
    *   If not included, skip binary files.
*   **Output Format:** Concatenate included file contents using the strict format:
    ```
    File: [Full Path]
    -----------------
    [Content or Base64 String]
    -----------------

    ```
    (Ensure two newlines separate entries).
*   **Display:** Show the final string in a read-only `<textarea>`.
*   **Copy Functionality:** Include a button to copy the textarea content to the clipboard.
*   **UI:** 
    * Use semantic HTML5 structure (`<header>`, `<main>`, `<section>`, `<footer>` as appropriate).
    * Include a descriptive `<title>` and `<meta name="description">` for SEO.
    * Add clear explanatory text sections: what the tool does, why it's useful, and how to use it.
    * Clean, professional, and responsive layout using CSS Flexbox or Grid.
    * Clearly separated ZIP and Folder input options, a single checkbox, status/error area, output area, and copy button.
*   **Feedback:** Provide status messages (e.g., "Processing ZIP...", "Processing Folder...", "Done!", error messages).
*   **Error Handling:** Handle invalid file types, ZIP processing errors, and folder read errors gracefully.

## 3. Technology Stack

*   HTML5 (including `webkitdirectory` attribute for folder input, semantic elements, and SEO tags)
*   CSS3 (with responsive design using Flexbox or Grid)
*   Modern JavaScript (ES6+, async/await)
*   JSZip library (via CDN: `https://cdnjs.cloudflare.com/ajax/libs/jszip/3.10.1/jszip.min.js`)
*   FileReader API (for folder file reading)

## 4. Scope & Constraints

*   **Client-Side Only:** Absolutely no server interaction for file processing.
*   **Single Page Application:** Deliverable as a single HTML file or clearly separated HTML/CSS/JS components intended to run as one page.
*   **Target User:** Users needing to prepare context from codebases or document sets within ZIP files or folders for LLM interaction using ContextPack.
