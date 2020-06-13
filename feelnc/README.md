## FEELnc

[FEELnc](https://github.com/tderrien/FEELnc) is a program to identify and classify new lncRNA. It is fast and accurate. This image is based on version 0.1.1 - [Paper](http://nar.oxfordjournals.org/content/early/2017/01/03/nar.gkw1306.full).

<u>Docker Pull Command:</u> `docker pull rcoan/feelnc`

### Usage

FEELnc has three modules runned separetly in a terminal window.

`docker run -w /mnt -v $(PWD):/mnt --rm rcoan/feelnc FEELnc_filter.pl <OPTIONS> > <OUTPUT_FILE>`

`docker run -w /mnt -v $(PWD):/mnt --rm rcoan/feelnc FEELnc_codpot.pl <OPTIONS>`

`docker run -w /mnt -v $(PWD):/mnt --rm rcoan/feelnc FEELnc_classifier.pl <OPTIONS> > <OUTPUT_CLASSES.TXT>`

All options found in the manual can be added.

The above commands mount your current directory to the container.
