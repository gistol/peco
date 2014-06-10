go-percol
======

(VERY ALPHA) Port of percol to Go

Installation
============

```
go get github.com/lestrrat/percol/cmd/percol/
```

Usage
=====

Use with [ghq](https://github.com/motemen/ghq) to select/display the godoc for your work in your GOPATH

```
godoc $(ghq list --full-path | percol --query $QUERY) | $PAGER
```

TODO
====

Test it. In doing so, we may change the repo structure

Break things up into separate goroutines to handle terminal drawing and user-input handling

Implement all(?) of the original percol options

Pagination

Notes
=====

Much code stolen from https://github.com/mattn/gof
Currently can only search by entering characters, and then when you have 1 entry, you can press enter to print the selected line, which you can feed to another command

Example:

```
ps aux | percol
```

Then try typing the PID of some running process, then press enter.