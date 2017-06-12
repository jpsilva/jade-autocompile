# slm-autocompile package [![Build Status](https://travis-ci.org/jpsilva/slm-autocompile.svg?branch=master)](https://travis-ci.org/jpsilva/slm-autocompile) [![apm](https://img.shields.io/apm/dm/slm-autocompile.svg)](https://atom.io/packages/slm-autocompile) [![apm](https://img.shields.io/apm/v/slm-autocompile.svg)](https://atom.io/packages/slm-autocompile)

Auto compile slm files on save

[Atom package site](https://atom.io/packages/slm-autocompile)

## Configuration
The two first comment blocks of file can be used to pass parameters to the compiler.

* The first one must have the name of the output html file, like this:

  ```slm
  / output: output.html
  ```
  If you avoid this comment, the file is omitted by the compiler.

  The output parameter supports relatives paths and two variables replacement.
  * $1: Name of the original slm file
  * $2: Extension of the original file.

  e.g. The following line will compile about.slm to about/index.html

  ```slm
  / output: $1/index.html
  ```

* The second block can have a javascript object to be used as locals for the compiler.

  ```slm
  / {
      name: 'Manuel',
      date: new Date,
      myFunc: function(){
        return true;
      }
    }
  ```

## Slm Language

Checkout the slm-lang README: https://github.com/slm-lang/slm

## About this Package

This package was forked from jade-autocompile Atom extension by Manuel Rueda: https://github.com/ManRueda/jade-autocompile

## License
  The MIT License (MIT)

  Copyright (c) 2017 Justin Silva

  Permission is hereby granted, free of charge, to any person obtaining a copy
  of this software and associated documentation files (the "Software"), to deal
  in the Software without restriction, including without limitation the rights
  to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
  copies of the Software, and to permit persons to whom the Software is
  furnished to do so, subject to the following conditions:

  The above copyright notice and this permission notice shall be included in all
  copies or substantial portions of the Software.

  THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
  IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
  FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
  AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
  LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
  OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
  SOFTWARE.
