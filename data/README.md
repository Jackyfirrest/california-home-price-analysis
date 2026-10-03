# Data

`raw/California/` contains the 15 requested monthly CRMLS files from February 2025 through April 2026.

The notebook reads this exact date range. It keeps the raw files unchanged and skips July 2025 because that source CSV is incomplete.

Files outside the requested period and duplicate downloads are stored in `../archive/` and are not used.
