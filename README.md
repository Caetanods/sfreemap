### Package Requirements for Production

You need to have R installed on your system, plus some dependencies. If you are using a debian/ubuntu based distribution, just type the following command in a terminal.

`sudo apt-get install r-base-core libblas-dev liblapack-dev`

### Package Requirements for Development

```
# On Fedora libssl-dev might be called libssh2-devel, and on OS X might be just libssh2
sudo apt-get install r-base-core texlive-full zlib1g-dev libcurl4-openssl-dev libssl-dev
```

### Install

```
install.packages('devtools')
require(devtools)
install_github('dpasqualin/sfreemap')
```

If you have troubles installing the `devtools` package, try cloning
`sfreemap` and then installing it, with the following commands:

```
git clone https://github.com/dpasqualin/sfreemap.git
R CMD build sfreemap && R CMD INSTALL sfreemap
# Vignettes will be available in the directory `sfreemap.Rcheck`.
```

Some people might have problems with package `Briostrings` as well, which is
a dependency of `phangorn`, which is a dependency of `sfreemap`. If you do,
the official Biostrings website suggest the following commands to install
it:

```
## try http:// if https:// URLs are not supported
source('https://bioconductor.org/biocLite.R')
biocLite('Biostrings')
```

### Help and Vignettes

If you want to look at the reference manual, load R and type the following
commands. A new tab will open in your web browser with the description of
all available functions.

```
require(sfreemap)
help(package = "sfreemap", help_type = "html")
```

The following command will open a new tab in your web browser with a link to
the vignettes (HTML).

```
browseVignettes("sfreemap")
```
