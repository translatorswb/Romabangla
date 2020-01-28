Romabangla
========



A simple rule-based transliteration tool to convert Latin script to Bengali script. 

## Requirements ##
* Gcc compiler with support for Unicode

## How to use ##

* Compile using the makefile in the Backend-source directory, then run using
```
./translpsl "Skula"
```
Output:
```
স্কুল
```
You may have to strip down diacritics from the input text first; there are many ways to do so, eg. using _iconv_ like so
```
./translpsl `echo "Barṇamālā" | iconv -f utf8 -t ascii//TRANSLIT`

```
Output:
```
বর্নমল
```
(This is of course incorrect Bengali but can still be useful)
