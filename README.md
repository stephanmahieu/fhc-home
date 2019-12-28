# fhc-home
Github pages repository for [Form History Control](https://stephanmahieu.github.io/fhc-home/)

## docs
Static html generated by [mkdocs](https://www.mkdocs.org/), this is the acual github pages repository.

The github pages url is: https://stephanmahieu.github.io/fhc-home/

## docsource
The directory containing the documentation source markdown files.

### Generate the site
From the same directory as the mkdocs.yml configuration file:

     mkdocs build --clean

### Test the site locally
From the same directory as the mkdocs.yml configuration file:

     mkdocs serve -a localhost:8080

## downloads
This is where binaries are stored that are made available for download.

## mkdocs Installation
    # supported python versions <= 3.7.x
    scoop install python
    python -m pip install --upgrade pip
    pip install mkdocs
    pip install mkdocs-material

### install older python version
    # add the 'versions' bucket if you haven't already
    scoop bucket add versions
    
    scoop install python37
    scoop reset python37