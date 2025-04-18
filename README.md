# ContextPack

**ContextPack** is a free, client-side web tool that lets you upload a ZIP archive or a folder, preview and select files/folders in an interactive tree, and generate a single, LLM-ready text block from your selection. All processing is done in your browser—no files are ever uploaded.

## Features

- **ZIP or Folder Input:** Upload a `.zip` archive or select a local folder (including subfolders).
- **Interactive File Tree:** Preview your input as a collapsible tree (powered by jsTree) with tri-state checkboxes for easy selection/deselection of files and folders.
- **Selection Statistics:** See real-time stats for total files, folders, input size, and your current selection.
- **Client-Side Processing:** All processing is done in your browser. No files are uploaded to any server.
- **Text and Binary Handling:** Text files are included as UTF-8. Optionally include binary files (e.g., images) as Base64.
- **LLM-Ready Output:** Concatenates all selected file contents in a strict, repeatable format for easy LLM prompt use.
- **Copy/Download Output:** One-click copy or download of the output, with the filename based on your input.
- **Responsive UI:** Clean, modern, and mobile-friendly interface.

## Why use ContextPack?

- **LLM/AI Prompting:** Quickly package your codebase or documentation for use as context in LLMs or AI coding assistants.
- **Documentation & Analysis:** Generate a single text file for documentation, code review, or text analysis tools.
- **Version Comparison:** Compare the textual content of different codebase versions easily.
- **Privacy & Speed:** All processing is done in your browser—no files are uploaded to any server.

## How to Use

1. **Select Input:** Click "ZIP File" or "Folder" to upload a `.zip` archive or select a local folder.
2. **Preview & Select:** After loading, an interactive file tree will appear. Use the checkboxes to select or deselect files and folders. The tree starts collapsed; click folders to expand.
3. **Review Statistics:** The stats panel shows the total files, folders, and size of your input, as well as your current selection.
4. **Include Binary Files:** Optionally, check "Include non-text files (as Base64)" to include binary files (e.g., images) as Base64 strings.
5. **Generate Output:** Click "Generate Context Pack from Selection" to process only the checked files. Progress will be shown.
6. **Copy or Download:** When done, copy the output to your clipboard or download it as a text file (filename is based on your input).

## License

This project is licensed under the [MIT License](LICENSE).

---

&copy; 2025 ContextPack. All processing is client-side. No files are uploaded.
