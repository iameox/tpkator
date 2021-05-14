# TPKator
Extract data from Club Penguin's Card-Jitsu Snow .tpk files.

## Installation
It's just 2 Bash files.
You need `imagemagick` (`convert` and `identify`), `jq` and `perl` installed.  
I tested it on WSL Ubuntu 18.04 (ImageMagick 7.0.11-8, Perl 5.26.1, jq 1.5-1).

## Launch
```bash
./extract <infile> # Tries to retrieve data from <infile>.
                   # The file sections (t, j, i, etc.) are extracted to sections/.
                   # The frames are converted to PNG and stored in frames/.

./tpkator <indir> <outdir> # Tries to extract data from the files of <indir> and append all the frames of one image together.
                           # The generated spritesheet is stored in <outdir> (the folder structure is kept).
                           # Image data is written to <outdir>/images.json at the end of the script (see below).
```
## Structure of images.json
```json
{
  "images": [
    {
      "file": "spritesheet location in <outdir>",
      "count": "number of sprites in spritesheet",
      "width": "sprite width",
      "height": "sprite height",
      "interval": "sprite duration in ms (1000/interval = framerate)",
    }
  ]
}
```
