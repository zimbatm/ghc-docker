Docker + Ubuntu 12.04 + GHC 7.8.4
=================================

It's all in the title

Usage
-----

This container can be used to build Haskell binaries.

Example of a Dockerfile:
```
FROM zimbatm/ghc
WORKDIR /src
ADD . /src
RUN cabal sandbox init
RUN cabal update && cabal install --only-dependencies --enable-tests -j
```
