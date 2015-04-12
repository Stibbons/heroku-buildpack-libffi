Heroku buildpack: cffi
========================

Use this buildpack with multipack if you have the following issue:

    building '_cffi_backend' extension
    creating build/temp.linux-x86_64-2.7
    creating build/temp.linux-x86_64-2.7/c
    gcc -pthread -fno-strict-aliasing -g -O2 -DNDEBUG -g -fwrapv -O3 -Wall -Wstrict-prototypes -fPIC -DUSE__THREAD -I/usr/include/ffi -I/usr/include/libffi -I/app/.heroku/python/include/python2.7 -c c/_cffi_backend.c -o build/temp.linux-x86_64-2.7/c/_cffi_backend.o
    c/_cffi_backend.c:13:17: fatal error: ffi.h: No such file or directory

File .buildpacks:

    https://github.com/Stibbons/heroku-buildpack-libffi.git
    backend=https://github.com/heroku/heroku-buildpack-python.git
    frontend=https://github.com/heroku/heroku-buildpack-nodejs
