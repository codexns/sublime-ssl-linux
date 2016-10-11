# sublime-ssl-linux

This is a Sublime Text dependency that adds a custom `_ssl` shared
library to the following versions of Sublime Text:

 - ST2 on Linux (x32 and x64)
 - ST3 (build 3108 or older) on Linux (x32 and x64)

The reason this dependency is necessary is because different distributions of
Linux ship different versions of OpenSSL that are linked using different names.
This dependency includes shared library shims for:

 - libssl-1.0.0
 - libssl-10
 - libssl-0.9.8

In addition, a custom loader is included that tries importing the shims in that
order until one loads properly.
