# LJNormalize
### Normalize .csv's similarly to the LJ Speech Dataset

Normalize and format data in .csv's in a way that mimics the LJ Speech Dataset. This script is intended to be used in conjunction with `srt-parse.py` (see https://github.com/cubrink/srt-parse)

### Usage

    usage: LJNormalize [-h] [--overwrite OVERWRITE] [--out-filename OUT_FILENAME]
                       [--in-encoding IN_ENCODING] [--out-encoding OUT_ENCODING]
                       [--csv-seperator CSV_SEPERATOR]
                       [--log-troublesome LOG_TROUBLESOME] [--log-name LOG_NAME]
                       input

    Normalize text data in csv similarly to the LJSpeech dataset

    positional arguments:
      input                 Location of .csv file to be normalized

    optional arguments:
      -h, --help            show this help message and exit
      --overwrite OVERWRITE
                            Write directly to the input file
      --out-filename OUT_FILENAME
                            Name of file to write to
      --in-encoding IN_ENCODING
                            Encoding to use when reading the .csv
      --out-encoding OUT_ENCODING
                            Encoding to use when writing to .csv
      --csv-seperator CSV_SEPERATOR
                            Character to used to seperate csv columns
      --log-troublesome LOG_TROUBLESOME
                            Create a log file listing lines with difficult
                            characters to normalize.
      --log-name LOG_NAME   Name of log file

### Known problems
- Currently lines using currency symbols (e.g. `$`) are detected but not normalized. The location of these symbols are noted in the log file (`troublesome.log` by default)

- Roman numerals are *not* currently detected or logged. If any are present in the input `.csv`, they will need to be found and normalized manually.

#### Reference 
For reference, the LJ Speech Dataset can be accessed at
https://keithito.com/LJ-Speech-Dataset/
