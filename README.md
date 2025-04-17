# ContextPack

**ContextPack** is a free, client-side web tool that converts the contents of a ZIP file or a local folder into a single, flat text block. This makes it easy to provide project context to Large Language Models (LLMs) and AI coding assistants.

## Features

- **ZIP or Folder Input:** Upload a `.zip` archive or select a local folder (including subfolders).
- **Client-Side Processing:** All processing is done in your browser. No files are uploaded to any server.
- **Text and Binary Handling:** Text files are included as UTF-8. Optionally include binary files (e.g., images) as Base64.
- **LLM-Ready Output:** Concatenates all file contents in a strict, repeatable format for easy LLM prompt use.
- **Copy to Clipboard:** One-click copy of the output for use in prompts or documentation.
- **Responsive UI:** Clean, modern, and mobile-friendly interface.

## Why use ContextPack?

- **LLM/AI Prompting:** Quickly package your codebase or documentation for use as context in LLMs or AI coding assistants.
- **Documentation & Analysis:** Generate a single text file for documentation, code review, or text analysis tools.
- **Version Comparison:** Compare the textual content of different codebase versions easily.
- **Privacy & Speed:** All processing is done in your browser—no files are uploaded to any server.

## How to Use

1. **Select ZIP File:** Click "Select ZIP File" to upload a `.zip` archive.
2. **Select Folder:** Or click "Select Folder" to process a local folder (including subfolders).
3. **Include Binary Files:** Optionally, check "Include non-text files (as Base64)" to include binary files as Base64 strings.
4. **Copy Output:** Wait for processing. The output will appear in a large text area. Click "Copy to Clipboard" to copy the result.

## License

This project is licensed under the [MIT License](LICENSE).

---

&copy; 2025 ContextPack. All processing is client-side. No files are uploaded.
