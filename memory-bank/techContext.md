# Tech Context: ContextPack

## Technologies Used

- **HTML5:** Markup for the ContextPack single-page application, including the `webkitdirectory` attribute for folder input, semantic elements (`<header>`, `<main>`, `<section>`, `<footer>`), and SEO tags (`<title>`, `<meta name="description">`).
- **CSS3:** Embedded styles for layout, readability, and responsive design using Flexbox/Grid and media queries.
- **JavaScript (ES6+):** All logic, using modern features (async/await, arrow functions, etc.).
- **JSZip:** Client-side ZIP decompression, included via CDN (`https://cdnjs.cloudflare.com/ajax/libs/jszip/3.10.1/jszip.min.js`).
- **FileReader API:** For reading files from folder input.

## Development Setup

- No build tools or bundlers required.
- Runs as a standalone HTML file in any modern browser.
- No server or backend setup needed for ContextPack.

## Technical Constraints

- **Client-Side Only:** All processing must occur in the browser; no data is sent to any server.
- **File Size:** Performance may degrade with very large ZIP files, folders, or many large binary files.
- **File Type Detection:** Relies on file extensions, which may not always be accurate.
- **Folder Input:** Uses the non-standard but widely supported `webkitdirectory` attribute for folder selection.

## Dependencies

- **JSZip** (CDN): For reading and extracting ZIP archives in the browser.

## Tool Usage Patterns

- **FileReader API:** Reads uploaded ZIP file as ArrayBuffer and reads files from folder input as text or Base64 (via DataURL).
- **JSZip API:** Loads and iterates ZIP contents.
- **navigator.clipboard:** Copies output to clipboard.
- **DOM Manipulation:** Updates UI elements and status messages.
- **Responsive CSS:** Uses Flexbox/Grid and media queries for layout and adaptability.
