# SSS (SAS, SPSS, Stata) → CSV
> Convert [`.sas7bdat`](https://documentation.sas.com/doc/en/pgmsascdc/9.4_3.5/hostwin/n0sk6o15955yoen19n9ghdziqw1u.htm#n19rscz36w9ly5n1c6bhrh8o348x), [`.sav`](https://www.ibm.com/docs/en/spss-statistics/26.0.0?topic=files-spss-statistics-data) or [`.dta`](https://www.loc.gov/preservation/digital/formats/fdd/fdd000471.shtml) to [`.csv`](https://en.wikipedia.org/wiki/Comma-separated_values) in Google Drive using Colab's R kernel  
> You only need a web browser and Google account; no need for proprietary software

- Flat: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/woncoh1/sss2csv/blob/main/sss2csv_flat.ipynb)
- Nested: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/woncoh1/sss2csv/blob/main/sss2csv_nested.ipynb)

## Intro
- This notebook uses Colab's R kernel to convert `.sas7bdat`, `.sav` or `.dta` files into `.csv` files
- All files are stored in Google Drive
- All metadata are discarded; only column names and data values are kept
- The input files can be moved to trash or left intact

## Folder structure
Upload files to Google Drive according to one of the following structures:  
(`.sav` or `.dta` may substitute `.sas7bdat` below)
1. Flat
    - **Main Folder**
        - `.sas7bdat` 1
        - `.sas7bdat` 2
        - ...
        - `.sas7bdat` n
2. Nested
    - **Main Folder**
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

## File permission
- Upload `.csv`: **editor** of the **main folder**
- Trash `.sas7bdat`, `.sav` or `.dta`: **owner** of the **file**

## Character encoding
- `.sas7bdat`, `.sav` or `.dta`
    - [cp949](https://en.wikipedia.org/wiki/Unified_Hangul_Code) (default)
    - [euc-kr](https://en.wikipedia.org/wiki/Extended_Unix_Code#EUC-KR)
    - [utf-8](https://en.wikipedia.org/wiki/UTF-8)
    - [latin1](https://en.wikipedia.org/wiki/ISO/IEC_8859-1)
- `.csv`: [utf-8](https://en.wikipedia.org/wiki/UTF-8) (default)

## TODO
Additional feature or bugfix request welcomed!
- [ ] Add more character encodings
- [ ] Extract, don't discard, metadata to CSV
- [ ] Improve time complexity with [concurrency](https://cran.r-project.org/web/packages/promises/vignettes/intro.html), parallelism, or distributed computing
