# OHMS XML to Markdown Transcript Converter

Convert Aviary OHMS XML transcript files to clean, formatted markdown documents.

## Features

- 📁 Upload XML files via drag-and-drop or file browser
- 🔄 Converts OHMS VTT transcripts to Q&A format
- 📝 Generates markdown matching oral history formatting standards
- ⬇️ Download as .md file
- 👀 Preview before downloading

## Usage

### Option 1: Open Directly in Browser

1. Open `index.html` in your web browser
2. Drag and drop your XML file or click to browse
3. Preview the generated markdown
4. Click "Download Markdown" to save the .md file

### Option 2: Run with Local Server

If you prefer to run a local server:

```bash
# Using Python 3
python -m http.server 8000

# Or using Python 2
python -m SimpleHTTPServer 8000

# Or using Node.js http-server
npx http-server
```

Then open `http://localhost:8000` in your browser.

## Input Format

Expects Aviary OHMS XML files with:
- Standard OHMS metadata fields (title, interviewee, interviewer, date, etc.)
- VTT transcript with speaker tags (e.g., `<v Q>`, `<v BURKAT>`)

## Output Format

Generates markdown with:
- Title page
- Abstract
- Restrictions, Format, and Transcript metadata sections
- Bibliography and citation forms
- Full transcript in Q&A format with speaker labels

## Structure

```
xml-to-markdown-transcript/
├── index.html          # Complete app (HTML + JavaScript)
├── README.md          # This file
├── example-xml.xml    # Example input file
└── example-pdf.pdf    # Target format reference
```

## Browser Compatibility

Works in all modern browsers that support:
- File API
- DOMParser for XML
- ES6 JavaScript

## Notes

- No server required - runs entirely in the browser
- No data is uploaded to any server - all processing is client-side
- Large files may take a moment to process

## License

Creative Commons CC BY-NC 4.0
