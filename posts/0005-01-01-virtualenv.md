---
title: Virtual ENV 
author: D
---

ひとつのシステム内に独立した複数の開発環境を構築

### install
```
$ pip install virtualenv
$ source ~/.zshrc
$ virtualenv --version
16.6.0
$ 
```

### create env
```
$ virtualenv env1
$ ls
env1

$ virtualenv -p python3.6 env2
```

### activate
```
$ source env2/bin/activate
(env2) $ 
```

### deactivate
```
$ deactivate
```

### path
```
$ which python
/Users/dongri/.pyenv/shims/python

$ source env2/bin/activate
$ which python
/Users/dongri/Desktop/virtualenv-test/env2/bin/python
$ 
```

### python2
```
$ pyenv install 2.7.16

ERROR: The Python zlib extension was not compiled. Missing the zlib?

Please consult to the Wiki page to fix the problem.
https://github.com/pyenv/pyenv/wiki/Common-build-problems


BUILD FAILED (OS X 10.14.5 using python-build 20180424)

Inspect or clean up the working tree at /var/folders/pj/t44ymwgn283bns9qtbysr5340000gn/T/python-build.20190612103656.26415
Results logged to /var/folders/pj/t44ymwgn283bns9qtbysr5340000gn/T/python-build.20190612103656.26415.log

$ sudo installer -pkg /Library/Developer/CommandLineTools/Packages/macOS_SDK_headers_for_macOS_10.14.pkg -target /
installer: Package name is macOS_SDK_headers_for_macOS_10.14
installer: Installing at base path /
installer: The install was successful.

$ pyenv install 2.7.16

$ pyenv versions
  system
  2.7.16
* 3.6.8 (set by /Users/dongri/.pyenv/version)
```

### use python2
```
$ virtualenv -p python2.7 env3
Running virtualenv with interpreter /Users/dongri/.pyenv/shims/python2.7
pyenv: python2.7: command not found

The `python2.7' command exists in these Python versions:
  2.7.16

$ pyenv global
3.6.8
$ pyenv global 3.6.8 2.7.16

$ pyenv global
3.6.8
2.7.16

$ virtualenv -p python2.7 env3
$ source env3/bin/activate
(env3) $ python -V
Python 2.7.16
(env3) $ which python
/Users/dongri/Desktop/virtualenv-test/env3/bin/python
```

