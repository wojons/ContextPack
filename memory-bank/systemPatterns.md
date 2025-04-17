# System Patterns: ContextPack

## System Architecture

- **Single-Page Application (SPA):** All logic and UI for ContextPack are contained within a single HTML file, with embedded CSS and JavaScript.
- **Semantic HTML Structure:** Uses `<header>`, `<main>`, `<section>`, and `<footer>` for clear content organization and accessibility.
- **SEO Integration:** Includes `<title>` and `<meta name="description">` for search engine discoverability.
- **Client-Side Only:** No server-side code; all processing is performed in the browser.
- **Library Integration:** Uses JSZip (via CDN) for ZIP decompression, and FileReader API for folder file reading.

## Key Technical Decisions

- **File Type Detection:** Uses file extensions to distinguish between text and binary files.
- **Binary Handling:** Binary files are Base64-encoded if included, otherwise skipped.
- **Output Formatting:** Strict, repeatable format for each file to maximize LLM context utility.
- **Asynchronous Processing:** Uses async/await for file reading, ZIP extraction, and folder file reading to ensure UI responsiveness.
- **Input Flexibility:** Supports both ZIP file input and folder input using the `webkitdirectory` attribute.

## Design Patterns

- **Event-Driven UI:** User actions (ZIP file input, folder input, checkbox, copy button) trigger processing and UI updates.
- **Progressive Enhancement:** Graceful error handling and status updates for better UX.
- **Separation of Concerns:** UI, processing logic, and status management are modularized within the script.
- **Responsive Design:** Uses CSS Flexbox/Grid and media queries to ensure usability on all devices.
- **Explanatory Content:** Dedicated sections for tool description, use cases, and instructions.

## Component Relationships

- **ZIP File Input** triggers ZIP processing.
- **Folder Input** triggers folder processing using `webkitdirectory` and `FileReader`.
- **Checkbox** controls binary file inclusion for both input types.
- **Status Area** displays feedback.
- **Textarea** displays output.
- **Copy Button** copies output to clipboard.

## Critical Implementation Paths

1. User selects ZIP file → Validate → Read as ArrayBuffer.
2. JSZip loads archive → Iterate files.
3. For each file: Detect type → Read as string or Base64 (if included) → Format output.
4. Concatenate all outputs → Display in textarea.
5. Copy button copies textarea content.

OR

1. User selects folder → Get FileList with `webkitdirectory` → Iterate files.
2. For each file: Use `webkitRelativePath` for path, detect type → Read as string (FileReader) or Base64 (FileReader + DataURL) → Format output.
3. Concatenate all outputs → Display in textarea.
4. Copy button copies textarea content.
