# Website

Source code for my website.

## Testing Locally

The steps below were influenced by [this post](https://michaelriedl.com/2021/06/11/testing-jekyll.html) (I had trouble following GitHub's default [guides/tutorials](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll)).

1. On MacOS, install ruby with homebrew: `brew install ruby`
1. Follow the ruby post-install steps/recommendations given by homebrew (i.e., set a few environment variables in your `.zshrc`)
1. Start a new shell session, and check that `gem` and `bundler` are installed through the ruby homebrew install:
    ```
    $ which ruby
    /opt/homebrew/opt/ruby/bin/ruby

    $ which gem
    /opt/homebrew/opt/ruby/bin/gem

    $ which bundler
    /opt/homebrew/opt/ruby/bun/bundler
    ```
1. Install gems/configure the project in a local `vendor/bundle` directory:
    ```
    bundle install --path vendor/bundle
    ```
1. Deploy website locally:
    ```
    bundle exec jekyll serve
    ```

Make sure the `github-pages` gem is up to date so that what I am previewing locally matches what is actually pushed to the site (more info [here](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll#updating-the-github-pages-gem)).
