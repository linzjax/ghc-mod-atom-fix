# ghc-mod-atom-fix
Since there's still not support for `gch-mod` to work with GHC 8.2.1, this is a stack.yaml configuration that makes it work in Atom.

Make sure your resolver is set to:
```
resolver: lts-11.17
```

Add the following to `extra-deps` in `stack.yaml`:

```
extra-deps:
  - https://hackage.haskell.org/package/ghc-mod-5.9.0.0/candidate/ghc-mod-5.9.0.0.tar.gz
  - cabal-helper-0.8.0.2
  - extra-1.5.3
  - monad-journal-0.7.2
  - optparse-applicative-0.13.2.0
  - either-4.4.1.1
  - free-4.12.4
  - haskell-src-exts-1.19.1
  - hlint-2.0.9
  - haskell-src-exts-util-0.2.1
```

Then run:
```
$ stack build ghc-mod
```

and suddenly the Haskell linter in Atom should start working again.
