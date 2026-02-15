# OHMS XML to Markdown Transcript Converter

Convert Aviary OHMS XML transcript files to clean, formatted markdown documents.

## Features

- 📁 Upload XML files via drag-and-drop or file browser
- 🔄 Converts OHMS VTT transcripts to Q&A format
- 📝 Generates markdown matching oral history formatting standards
- ✨ **Smart italics detection** for book/publication titles
- 📚 Custom title dictionary with browser storage
- 🔍 Preview detected titles before download
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
- Automatic italics formatting for book/publication titles

## Italics Feature

The app intelligently detects and italicizes book and publication titles using a hybrid approach:

### Automatic Pattern Detection

Automatically detects titles after phrases like:
- "the book", "the novel", "the memoir"
- "wrote", "published", "authored"
- "the journal", "the magazine", "the newspaper"
- "in [Publication Name]"

Plus recognizes major publications:
- The New York Times, The Washington Post, The Wall Street Journal
- The Atlantic, The New Yorker, Time Magazine
- Academic journals (Nature, Science, JAMA, The Lancet, etc.)

### Custom Title Dictionary

Add your own titles in the "Italics Settings" section:
- One title per line
- Saved to browser storage
- Exact match search (case-insensitive)
- Works across all future conversions

### Preview

Before downloading, see all detected titles that will be italicized, allowing you to verify the results.

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
