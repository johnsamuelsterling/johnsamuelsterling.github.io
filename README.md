# Website

```
This website is based on Dominik Moritz's design (https://github.com/domoritz/domoritz.github.io). Additionally, it takes inspiration from John Cobb's alterations to the prexisting template (https://github.com/johndcobb/johndcobb.github.io).
```

## Write

```
bundle exec jekyll post "My New Post"
```

## Run

```
bundle exec jekyll serve --livereload
```

## Run with Docker

```
docker run \
  --volume="$PWD:/srv/jekyll" \
  -p 4000:4000 -p 35729:35729 \
  -it jekyll/jekyll \
  jekyll serve --livereload
```
