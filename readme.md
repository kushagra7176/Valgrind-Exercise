# C++ Boilerplate
[![Build Status](https://travis-ci.com/kushagra7176/Valgrind-Exercise.svg?branch=master)](https://travis-ci.com/kushagra7176/Valgrind-Exercise)
[![Coverage Status](https://coveralls.io/repos/github/kushagra7176/Valgrind-Exercise/badge.svg?branch=master)](https://coveralls.io/github/kushagra7176/Valgrind-Exercise?branch=master)
---

## Overview

Valgrind Exercise

## Standard install via command-line
```
git clone --recursive https://github.com/kushagra7176/Valgrind-Exercise
cd <path to repository>
mkdir build
cd build
cmake ..
make
Run tests: ./test/cpp-test
Run program: ./app/shell-app
```

## How to use Valgrind
```
cd <path to repository>
cd build/app
valgrind --leak-check=full --log-file="<ouputfile.extension>" ./shell-app 
valgrind --tool=callgrind  ./shell-app
kcachegrind <generated callgrind.out... file> 
```
## Building for code coverage (for assignments beginning in Week 5)
```
sudo apt-get install lcov
cmake -D COVERAGE=ON -D CMAKE_BUILD_TYPE=Debug ../
make
make code_coverage
```
This generates a index.html page in the build/coverage sub-directory that can be viewed locally in a web browser.

