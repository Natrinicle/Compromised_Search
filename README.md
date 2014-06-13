Compromised_Search
==================

Performs a series of parallel greps of a directory to find potentially compromised files

USAGE: compromised_search [OPTION] [DIRECTORY]
Search for compromised websites using search terms in /usr/local/bin/compromised_search_terms

-c|--color|--colour (never|always)      - Colorize output
-t|--threads x                          - Number of threads of grep to run. Can be expressed as a percentage of cores (default 150%)
-d|--debug                              - Echo out search command, don't run it

Examples:
Debug scanning home directory with 2 grep processes for each processor core and don't colorize output
compromised_search -d -t 200% -c never ~

Scan Stacey's home directory with 2 simultaneous greps
compromised_search -t 2 ~stacey


Compromised Search Terms are located in the same directory as the script and are formatted as one regular expression per line. The script will auto escape spaces and add pipes between the expressions.
