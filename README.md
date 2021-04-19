# TPKator
Extract data from Club Penguin's Card-Jitsu Snow .tpk files.

## Installation
It's just 2 Bash files.
You need `imagemagick` (`convert`), `jq` and `perl` installed.  
I tested it on WSL Ubuntu 18.04 (ImageMagick 7.0.11-8, Perl 5.26.1, jq 1.5-1).

## Launch
```bash
./extract <infile> # Tries to retrieve data from <infile>.
                   # The file sections (t, j, i, m, etc.) are extracted to sections/.
                   # The frames are converted to PNG and stored in frames/.

./tpkator <indir> <outdir> # Tries to extract data from the files of <indir> and append all the frames together.
                           # The generated spritesheet is stored in <outdir>/ (the folder structure is kept).
                           # The sprite sizes are written to sizes.txt.
```
