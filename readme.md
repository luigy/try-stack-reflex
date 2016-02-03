# try-stack-reflex

using `stack` latest `ghcjs` support to effortlessly compile `reflex-todomvc` 


## Setup

make sure you have installed `stack` >= 0.1.8  https://github.com/commercialhaskell/stack

``` sh
git clone https://github.com/luigy/try-stack-reflex
cd try-stack-reflex
```

### ghcjs-0.2 (aka improved-base)

```sh
stack setup
stack build
echo $(stack path --local-install-root)/bin/reflex-todomvc.jsexe/index.html
```

### ghcjs-0.1
```sh
./try-stack-reflex old
```
or
```sh
STACK_YAML=stack-ghcjs-old-base.yaml
stack setup
stack build

# path to generated index.html to open in you browser
echo $(stack path --local-install-root)/bin/reflex-todomvc.jsexe/index.html
```

### ghcjs --interactive
[video demo](https://cldup.com/K4Ub9rOl9V.mp4)
```sh
# vanilla ghcjs repo
./try-stack-reflex ghcjsi

# or a fork with ghcjsi support updated ~ 02/01/2016
./try-stack-reflex ghcjsi-fork
export NODE_PATH="$(pwd)/reflex-todomvc/node_modules"
cd reflex-todomvc
stack ghci

# open browser at localhost:6400
```

## Caveats

requires having `ghc` compiler in your `PATH` https://github.com/commercialhaskell/stack/issues/1258
