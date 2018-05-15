Inkscape (Dockerized for macOS)
============
[![](https://images.microbadger.com/badges/image/quar/inkscape.svg)](https://microbadger.com/images/quar/inkscape "Get your own version badge on microbadger.com")
[![](https://images.microbadger.com/badges/version/quar/inkscape.svg)](https://microbadger.com/images/quar/inkscape "Get your own version badge on microbadger.com")

#### Motivation:
Inkscape does not work on converting SVG to PDF on macOS 10.13 for the moment.
Installed through `brew cask install inkscape`, will throw "cannot find SVG, not valid SVG"
when converting SVG to PDF.

#### Version:
Inkscape 0.91 r13725

#### Usage:

```bash
cd $WORKING_DIRECTORY_WHERE_FILES_TO_BE_CONVERTED
docker run -v $PWD:/workdir quar/inkscape --file=input.svg --export-pdf=output.pdf
```

#### Note:

* (2018-05-15) base image `ubuntu:17.10` does not work, can install Inkscape,
  but will throw runtime error

* (2018-05-15) base image `alpine:3.7` does not work, can install Inkscape,
  but will throw runtime error (segmentation fault)
