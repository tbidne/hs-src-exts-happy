# hs-src-exts-happy

`haskell-src-exts-1.23.1` fails to build with `happy-2.2.1`, though it builds with `happy-2.2`. For example:

##### Building with cabal.good.project, with an old index-state that chooses `happy-2.2`.
```
$ cabal build --project-file cabal.good.project
<success>
```

##### Building with cabal.good.project, with a new index-state that chooses `happy-2.2.1`.
```
$ cabal build --project-file cabal.bad.project
...
<snip>
...
unused rules: 3
The grammar has 12 shift/reduce conflicts.
This is different from the number given in the expect directive
Error: [Cabal-7125]
Failed to build haskell-src-exts-1.23.1 (which is required by hs-src-exts-happy-0.1.0.0). See the build log above for details.
```
