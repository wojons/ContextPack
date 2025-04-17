# Product Context: ContextPack

## Why This Project Exists

Many users, especially those working with Large Language Models (LLMs), need to provide context from codebases or document sets. Manually extracting and formatting file contents from ZIP archives or folders is tedious and error-prone.

## Problems It Solves

- Eliminates the need for manual extraction and concatenation of file contents from ZIP archives or folders.
- Provides a consistent, LLM-friendly format for context ingestion.
- Handles both text and binary files, with user control over binary inclusion.
- Allows users to select either a ZIP file or an entire folder, increasing flexibility for different workflows.

## How It Should Work

- User uploads a `.zip` file or selects a folder via a simple web interface.
- ContextPack processes all files in the archive or folder, concatenating their contents in a strict, predictable format.
- Text files are included as UTF-8 strings; binary files can be optionally included as Base64.
- The result is displayed in a read-only textarea for easy review and copying.

## User Experience Goals

- Fast, client-side processing with no server dependency.
- Clear, minimal UI with obvious controls and feedback for both ZIP and folder input.
- Robust error handling and status updates.
- Output is easy to copy and ready for LLM prompt use.
- Professional, responsive layout that adapts to all devices.
- Explanatory content and instructions are provided for user clarity.
- Semantic HTML and SEO tags improve accessibility and discoverability.
