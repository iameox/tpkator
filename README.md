# TPKator
Extracts data from Club Penguin's Card-Jitsu Snow .tpk files.

## Installation
It's just 2 Bash files.
You need `imagemagick` (`convert`), `jq` and `perl` installed.

## Launch
```bash
./extract <infile> <outfile> # Tries to extract data from <infile> into <outfile>.

./tpkator <indir> <outdir> # Tries to extract data from the files of <indir> into <outdir>.
                           # The sprite sizes are written to the file `sizes.txt`.
                           # Keeps the folder structure.
```
