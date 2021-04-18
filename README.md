# TPKator
Extracts data from Club Penguin's Card-Jitsu Snow .tpk files.

## Installation
It's just 2 Bash files.
You need `imagemagick` (`convert`), `jq` and `perl` installed.
I tested it on WSL Ubuntu 18.04 (ImageMagick 7.0.11-8, Perl 5.26.1, jq 1.5-1).

## Launch
```bash
./extract <infile> <outfile> # Tries to extract data from <infile> into <outfile>.

./tpkator <indir> <outdir> # Tries to extract data from the files of <indir> into <outdir>.
                           # The sprite sizes are written to the file `sizes.txt`.
                           # Keeps the folder structure.
```
