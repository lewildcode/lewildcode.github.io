The LwcBlog
===========

This is our blog page.
To contribute, feel free to create PR's or [contact us](https://github.com/lewildcode/lewildcode.github.io/issues/new).

## Write posts

To create new blog posts, open up one of the existing posts in the [_posts folder](https://github.com/lewildcode/lewildcode.github.io/tree/master/_posts) to see
the required structure. You can use [markdown](http://daringfireball.net/projects/markdown/syntax) in your posts as well as [liquid extensions](https://github.com/mojombo/jekyll/wiki/liquid-extensions).

### Syntax highlighting

Supported via [pygments](http://pygments.org/)

    {% highlight php %}
    ... your code ...
    {% endhighlight %}

## How to test this on your local machine?

Checkout the project, cd into it and run a local server for testing:

    jekyll --server

The static pages will be generated and a http server is started on port 4000, thus point your browser to http://localhost:4000 to click through the site.
Please note that you'll need to install [pygments](http://pygments.org/) if you want syntax highlighting to work on your machine, otherwise it'll be just plain, unformated text.

### Install depenencies

    gem update --system
    gem install jekyll
    gem install rdiscount
