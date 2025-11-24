# ADIF Filter v1.0.0

A GUI utility written in Python to parse, filter, merge, and re-save ADIF (Amateur Data Interchange Format) log files.

Designed for amateur radio operators who need to combine logs from different sources, clean up unnecessary fields, or prepare logs for QSL managers and LoTW.

## Key Features

*   **Merge Multiple Logs:** Drag and drop multiple `.adi` / `.adif` files to combine them into a single output file (e.g., merge a contest log with your main logbook).
*   **Deduplication:** Automatically identifies and removes duplicate QSOs based on `CALL`, `BAND`, `MODE`, `QSO_DATE`, and `TIME_ON`.
*   **Field Filtering:** Select exactly which ADIF fields to keep (e.g., strip contest-specific fields like `APP_N1MM_...` while keeping essential QSO data).
*   **Drag & Drop Interface:** Intuitive visual drop zone for easy file loading.
*   **Grid Layout:** Multi-column view makes managing dozens of ADIF fields easy and readable.
*   **Configuration:** Remembers your selected fields between sessions via `adif_config.txt`.

## Requirements

*   Python 3.12 or newer
*   Dependencies listed in `requirements.txt`:
    *   `PyQt6`
    *   `chardet`

## Installation

1.  **Download Files**
    Download the `adif_filter.py` and `requirements.txt` files and save them together in a new folder on your computer (for example, a folder named `adif-filter`).

2.  **Install Dependencies**
    Open a terminal or command prompt, navigate into the folder where you saved the files, and run the following command:
    
```bash
pip install -r requirements.txt
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
