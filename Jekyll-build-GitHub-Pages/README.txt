1. Add the following to your project's Gemfile:  

gem 'github-pages', group: :jekyll_plugins

2. Run bundle install

Note: You are not required to install Jekyll separately. Once the github-pages gem is installed, you can build your site using jekyll build, or preview your site using jekyll serve. For more information about installing Jekyll locally, please see the GitHub Help docs on the matter.

https://github.com/github/pages-gem#github-pages-ruby-gem

- ERROR: bundler: failed to load command: jekyll

I stumbled upon this question when I ran into the issue of trying to set up github pages. It seems that in the latest version of ruby that is installed with homebrew webrick is not included by default. Here is the github issue: https://github.com/github/pages-gem/issues/752. Recommendations are to either use ruby 2.7 or to manually add webrick in using the command below:

(cd into project directory with gemfile)

bundle add webrick

and then repeating the command

bundle exec jekyll serve