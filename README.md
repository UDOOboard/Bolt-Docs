# UDOO Bolt Documentation

[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](https://github.com/UDOOboard/Bolt-Docs/LICENSE)

Travis build status: [![Build Status](https://travis-ci.org/UDOOboard/Bolt-Docs.svg?branch=master)](https://travis-ci.org/UDOOboard/Bolt-Docs)

This repository contains the source code for the documentation hosted at [www.udoo.org/docs-bolt/](http://www.udoo.org/docs-bolt/).


## Build the documentation locally
On PHP7+ install XML and mbstring modules:

    sudo apt install php7.2 composer php7.2-xml php7.2-mbstring
    composer install

Then build the documentation with

    composer generate && cp -r img/ static/

To serve the documentation from a development webserver, run

    cd static && php -S localhost:8080
