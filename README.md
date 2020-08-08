# dtn7.github.io

Repository for [dtn7.github.io](https://dtn7.github.io/), powered by GitHub Pages/Jekyll.


## Docker Container

```sh
# Build the container
docker build -t gh-pages-dtn7 .

# Update dependencies
docker run --rm -v "$PWD":/usr/src/app gh-pages-dtn7 bundle update

# Serve page on http://localhost:4000/
docker run -it --rm -v "$PWD":/usr/src/app -p "4000:4000" gh-pages-dtn7
```
