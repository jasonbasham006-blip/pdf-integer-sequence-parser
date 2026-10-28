# PDF Integer Sequence Parser

Universal Integer Sequence Pipeline Diagnostic Driver.

Exact consecutive integer sequence finder for PDF text extraction with zero-drift token parsing.

## Features

- Dual-engine PDF text extraction (`pdfplumber` primary, `pypdf` fallback)
- Precise numeric token isolation (integers, grouped integers, decimals, scientific notation)
- Exact consecutive integer sequence matching across pages
- Built-in mock/test mode when no PDF is supplied
- Auto-install of runtime dependencies on first run

## Requirements

- Python 3.10+
- `pypdf`
- `pdfplumber`

## Install

```bash
pip install -r requirements.txt
```

Or just run the script — it will auto-install missing packages on first launch:

```bash
python pdf_sequence_parser.py --test
```

## Usage

### Test mode (no PDF needed)

```bash
python pdf_sequence_parser.py --test
```

### Against a real PDF

```bash
python pdf_sequence_parser.py /path/to/your/document.pdf
```

### Output

JSON report with match status for the two built-in target sequences:

- `zero_based`
- `notebook_origin_603`

## License

MIT
