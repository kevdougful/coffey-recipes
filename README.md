# Coffey Family Recipe Book

## Contributing

Feel free to contribute. If you're a Github user and you already know how to contact me ([Twitter](https://twitter.com/kevdougful) works too), I'll go ahead and add you to the repo. Otherwise, [fork and PR](https://gist.github.com/Chaser324/ce0505fbed06b947d962). 

## Creating Content

This project is meant to be easy to maintain and deploy. If you're comfortable with command-line, git, and markdown, contributing content should be easy.

### Hugo

This project leverages [Hugo](https://gohugo.io) to generate static HTML that is then uploaded and served from a public S3 bucket. You don't really need Hugo to add content, but it does provide some nice utilities like [standing up a local server](https://gohugo.io/commands/hugo_server/) so you can double check that your markdown is looking how you intended before pushing to Github. You can view the install docs [here](https://gohugo.io/getting-started/installing/).

### Front Matter

Each recipe should be placed into [content/recipes](content/recipes) with a `.md` extension. There are a few items that should be placed at the beggining of each file that Hugo uses to generate certain elements of the site. See the example below for more information. In theory, you could write a few using Github's built-in markdown editor but I don't recommend it. [GFM](https://github.github.com/gfm/) does not always render exactly the same as Hugo, and running `hugo serve` on a local directory is always a good check before pushing to Github.

This is the basic format you should follow for each recipe

```
---
title: "Short name for the recipe. Probably no more than ten words"
summary: "A catchy describing the dish. Keep it within 1-3 sentences"
date: 2020-09-28T16:11:23-06:00
draft: false (if true, won't be rendered but will exist in the repository)
time: "1h"
tags: ["some", "short", "pertinent", "words"]
featured_image: "/imagename.png" (store it in static dir, make sure it's square <400px)
---

_Author: Author Name_

## Ingredients

- 1/2 cup Ingredient A
- 1.5 oz Ingredient B
- Some other stuff

## Directions

1. Step 1
2. Step 2
3. And so on...
```