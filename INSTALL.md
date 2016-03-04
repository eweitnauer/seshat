How to Install on OSX El Capitan (10.11.3)
==========================================

* clone seshat git repository
* install boost `brew install boost`
* ln -s /usr/include/limits.h /usr/local/include/values.h
* brew install xerces-c


EM-Scripten
===========

- install the portable SDK of [emscripten](http://kripken.github.io/emscripten-site/docs/getting_started/downloads.html#sdk-download-and-install)
- change `python2` in the first line of emsdk-dir/emscripten/1.35.0/em++ and emsdk-dir/emscripten/1.35.0/emxcc to `python`
- added `__x86_64__` definition to the Makefile to get around unsupported architecture problem
- replace g++ with em++ in Makefile
- run `emmake make`



==> next step:
everything seems to work except for the xerxces-c library -- I need to find out how to compile that separately with emmake and bind it to seshat
