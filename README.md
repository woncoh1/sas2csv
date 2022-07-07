# SAS → CSV
> Convert [`.sas7bdat`](https://documentation.sas.com/doc/en/pgmsascdc/9.4_3.5/hostwin/n0sk6o15955yoen19n9ghdziqw1u.htm#n19rscz36w9ly5n1c6bhrh8o348x) to [`.csv`](https://en.wikipedia.org/wiki/Comma-separated_values) in Google Drive using the R kernel for Google Colab  
> You only need a web browser and Google account; no need for proprietary software

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/woncoh1/sas2csv/blob/main/sas2csv.ipynb)

## Intro
- This notebook uses Colab's R kernel to convert `.sas7bdat` files into `.csv` files
- All metadata are discarded; only column names and data values are kept
- All `.sas7bdat` and `.csv` files are stored in Google Drive
- The `.sas7bdat` files can be moved to trash or left intact

## Folder structure
Upload files to Google Drive according to the following structure:
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
- Trash `.sas7bdat`: **owner** of the **main folder**

## Character encoding
- `.sas7bdat`
    - [cp949](https://en.wikipedia.org/wiki/Unified_Hangul_Code) (default)
    - [euc-kr](https://en.wikipedia.org/wiki/Extended_Unix_Code#EUC-KR)
    - [utf-8](https://en.wikipedia.org/wiki/UTF-8)
    - [latin1](https://en.wikipedia.org/wiki/ISO/IEC_8859-1)
- `.csv`: [utf-8](https://en.wikipedia.org/wiki/UTF-8) (default)

## TODO
Additional feature or bugfix request welcomed!
- [ ] Add more character encodings
- [ ] Expand to `.sav` (SPSS) and `.dta` (Stata) files
- [ ] Fix progress status message (list files using [purrr::map](https://purrr.tidyverse.org/reference/map.html) + [dplyr::bind_rows](https://dplyr.tidyverse.org/reference/bind.html))
- [ ] Consider using [progress bar](https://github.com/r-lib/progress)
- [ ] Add [interactive tibbles](https://glin.github.io/reactable/) for listing folders and files
- [ ] Check whether trashing requires owner permission for folder or file
- [ ] [Deploy](https://shiny.rstudio.com/deploy/) as [Shiny app](https://shiny.rstudio.com/)
- [ ] Improve time complexity
