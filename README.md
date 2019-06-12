# Install

```
# stack install hakyll --resolver lts-10.9
```

# Init
```
$ hakyll-init hazy

$ cd hazy
$ stack init
$ stack build
$ stack exec site build

$ stack exec site watch

$ open localhost:8000
```

# Deploy
```
$ git checkout -b gh-pages

$ site.hs 編集

$ stack build

$ stack exec site deploy
```
