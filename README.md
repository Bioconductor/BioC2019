This repository contains material for the _Bioconductor_ annual
conference. [View the conference web site][1].

Edit or add material as markdown files in the docs/ directory. Please
wrap lines to 80 character width and aim for simple markdown rather
than elaborate html or other content.

Please follow best practices by previewing changes locally. 

1. Make sure that ruby and bundler are installed, following the
   'Requirements' section of [GitHub's documentation][2].

2. Clone the repository and switch to the `docs/` directory

        cd BioC2018/docs

3. Install ruby pre-requisites.

        bundle install     # once only; references Gemfile
        
4. Execute the jekyll server

        bundle exec jekyll serve
        
    and view the results at https://localhost:4000

[1]: https://bioconductor.github.io/BioC2018.
[2]: https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/#requirements
