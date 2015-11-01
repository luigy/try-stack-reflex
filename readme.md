# try-stack-reflex

using `stack` latest `ghcjs` support to effortlessly compile `reflex-todomvc` 


## Setup

make sure you have installed `stack` >= 1.7 (not realeased yet) https://github.com/commercialhaskell/stack/commit/4797dedd12aedc661697625549c52de8d335ffaf

``` sh
git clone https://github.com/luigy/try-stack-reflex
cd try-stack-reflex
```


### ghcjs-0.1

```sh
# currently doing some custom patching for relaxing bounds for bifunctor package
./try-stack-reflex old
```

### ghcjs-0.2 (aka improved-base)

```sh
./try-stack-reflex
```

## Caveats

requires having `ghc` compiler in your `PATH` commercialhaskell/stack#1258
