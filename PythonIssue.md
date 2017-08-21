# Python issues

## relative and absolute import[https://blog.tankywoo.com/python/2013/10/07/python-relative-and-absolute-import.html]
The absolute_import is default in Python 3.x

relative string.py module, not the Python's standard string module
> python -m pkg.main

When absolute imports are default, import string will always find the standard library's version
It is preferable to begin writing
> from pkg import string


What is the sys.path(top-level) when you run the code?[https://stackoverflow.com/questions/33743880/what-does-from-future-import-absolute-import-actually-do]

>'''python
> #!/usr/bin/env python
> # -*- coding = utf-8 -*-
> from __future__ import absolute_import
> import string
> import sys
>
> print(string)
> print(sys.path[0])
> string.say_hello()

when run in bash
> python script.py

This will add pkg to the sys.path.  "import string" is supposed to follow the principle and should find the standard module, but it just find the top-level path and find "pkg", so the local package is imported

instead of using will not add pkg to path, but ''.
> python -m pkg.script

> n190-p52:pkg ruibotu$ python -m script
> module 'string' from 'string.pyc'>
>
> say hello

> n190-p52:pkg ruibotu$ python script.py
>
> <module 'string' from '/Users/ruibotu/Desktop/pkg/string.pyc'>
> /Users/ruibotu/Desktop/pkg
> say hello
