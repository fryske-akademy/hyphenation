# Hyphenation of West Frisian words

With this software West Frisian words can be hyphenated, i.e. divided into syllables. The software includes a script by which a model is generated that is trained on the Foarkarswurdlist (preferred word list) and can be used for hyphenation. Additionally, an R Shiny web application is included that does the actual hyphenation.

## Generating the model

The model can be generated with the script `script.R` which runs in R. Make sure that R is installed on your computer, see `https://cloud.r-project.org/`. You can run the script from command line by the command: `Rscript script.R`. The script requires Phonetisaurus to be installed, see `https://pypi.org/project/phonetisaurus/`.

The script reads the Foarkarswurdlist which is stored in the file `hyph-fkw.txt` and outputs the alignments in `corpus.txt` (is not used further) and the model in `hyph.fst`. Line 36 in the script can probably be omitted if your computer has a lot of RAM.

## Running the web app

The web app includes the file `app.R` and the folder `www`. The folder `www` includes the model `hyph.fst`. The app can be run locally in R or RStudio, or on a server with Shiny Server installed, see [Get your Shiny apps online](https://posit.co/products/open-source/shiny-server/). An online version of the app can be found [here](https://www.fa.knaw.nl/fa-apps/Hyph/).

##### Linux (Debian / Ubuntu) installs

Before running the script for the first time, enter the following commands in a terminal:<br>

`sudo apt install r-base-core`<br>
`sudo apt install libcurl4-openssl-dev`<br>
`sudo apt install libxml2`<br>
`sudo apt install libxml2-dev`<br>
`sudo apt install libssl-dev`<br>
`sudo apt install libpoppler-cpp-dev`<br>
`sudo apt install libjpeg-dev`<br>

## Contact

E-mail: `wheeringa [at] fryske-akademy [dot] nl`
