# `Py3memimporter`

## WARNING

The shellcode in this module is python version specific, please use the branch that corresonds to your version.

## Import _memimporter from shellcode

Enables importing the _memimporter c extension via shellcode into builtins

Once added, it allows you to leverage _memimporter to import other python c extensions from memory.

_memimporter is a component of the [py2exe](https://github.com/py2exe/py2exe) tool

## Basic Usage

### run to get _memimporter loaded into current namespace
```python
import py3memimporter
```

### This can be verified by either checking the builtins or testing a reference to _memimporter
```python
dir(__builtins__)
_memimporter
```

## Gotchas
This obviously isn't quite as polished as pymemimporter in that it just makes the _memimporter module available as a builtin, but this is an importable component to another repo I'll be adding in the future. Also in the near future, I'll add a repo that actually walks through how the shellcode was generated so no one has to go through what I did to get this to work the way I wanted it.

## Special Thanks
* [natesubra](https://github.com/natesubra) - As always, so many random questions answered
* [py2exe](https://github.com/py2exe) - Thanks for the _memimporter module
* [n1nj4sec](https://github.com/n1nj4sec) - For letting me know it was possible, though I would have just preferred notes XD
