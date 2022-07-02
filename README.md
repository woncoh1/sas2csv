# sas2csv
> Convert `.sas7bdat` to `.csv` in Google Drive using Google Colab R kernel

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/woncoh1/sas2csv/blob/main/sas2csv.ipynb)

## User Guide
- General
    - This notebook uses Colab's R kernel to convert `.sas7bdat` files into `.csv` files
    - All `.sas7bdat` and `.csv` files are stored in Google Drive
    - The `.sas7bdat` files can be moved to trash or left intact
- Default character encoding
    - `.sas7bdat`: [cp949](https://en.wikipedia.org/wiki/Unified_Hangul_Code)
    - `.csv`: [utf-8](https://en.wikipedia.org/wiki/UTF-8)
- File permission
    - Upload only: editor of the main folder
    - Upload and trash: owner of the main folder
- Folder structure
    - Main Folder
        - Subfolder 1
            - `.sas7bdat` 1
            - `.sas7bdat` 2
            - ...
            - `.sas7bdat` n
        - Subfolder 2
            - `.sas7bdat` 1
            - `.sas7bdat` 2
            - ...
            - `.sas7bdat` n
        - ...
        - Subfolder n
            - `.sas7bdat` 1
            - `.sas7bdat` 2
            - ...
            - `.sas7bdat` n
