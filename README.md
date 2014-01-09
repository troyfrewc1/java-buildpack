# Cloud Foundry Java Buildpack Documentation
This branch (`gh-pages`) is the source for the GitHub Pages-based documentation for the Cloud Foundry Java Buildpack.

## Development
The buildpack's documentation is primarily displayed using [GitHub Pages][].  During development it is often useful to be able to render the site locally during development to ensure that what is displayed is good before the changes are pushed.  Since GitHub Pages is based on [Jekyll][] this can be done with very little fuss.  To start the server, run the following commands from the root of the repository.

```bash
bundle install
bundle exec jekyll serve -w
open http://0.0.0.0:4000/java-buildpack/
```

## Contributing
[Pull requests][] are welcome; see the [contributor guidelines][] for details.

[contributor guidelines]: CONTRIBUTING.md
[GitHub Pages]: http://pages.github.com
[Pull requests]: http://help.github.com/send-pull-requests
[Jekyll]: http://jekyllrb.com
