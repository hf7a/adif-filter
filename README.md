# ADIF Filter

A GUI utility written in Python to parse, filter, merge, and re-save ADIF (Amateur Data Interchange Format) log files.

Designed for amateur radio operators who need to combine logs from different sources, clean up unnecessary fields, or prepare logs for QSL managers and LoTW.

## Key Features

- **Merge Multiple Logs:** Drag and drop multiple `.adi` / `.adif` files into a single output file.
- **Deduplication:** Automatically removes duplicate QSOs based on `CALL`, `BAND`, `MODE`, `QSO_DATE`, and `TIME_ON`.
- **Field Filtering:** Select exactly which ADIF fields to keep.
- **Drag & Drop Interface:** Easy file loading.
- **Grid Layout:** Multi-column field selection.
- **Configuration:** Remembers selected fields via `adif_config.txt`.

## Requirements

- Python 3.10+
- PyQt6

## Installation

Install PyQt6:

```bash
pip install PyQt6
```
## Usage

Once the dependencies are installed, run the application from your terminal or command prompt:

```bash
python adif_filter.py
```

1.  **Load Files:** Drag and drop one or more `.adi` files onto the window, or click **"Add Files..."**.
2.  **Filter Fields:** The program detects all unique ADIF fields. Uncheck the ones you want to remove.
    *   *Tip:* Use "Reset Selection" to revert to the standard set of fields (`BAND`, `CALL`, `FREQ`, `MODE`, `RST`, etc.).
3.  **Deduplicate:** Ensure the **"Remove Duplicates"** checkbox is selected if you want to filter out identical records.
4.  **Save:** Click **"Merge, Process and Save"** to generate your new, clean ADIF file.

## Configuration

The program automatically creates a file named `adif_config.txt` in the same directory. This file stores the list of fields you want to keep by default.

## Author

**[Leszek HF7A](https://www.qrz.com/db/HF7A)**

## License

This project is licensed under the **MIT License**.
