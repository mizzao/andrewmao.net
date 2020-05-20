Prereqs: https://jekyllrb.com/docs/installation/#requirements

- `gem install jekyll bundler`

- `bundle install` and `jekyll serve --watch`
- OR `bundle exec jekyll serve --watch`

Updating gems to match latest github-pages: `bundle update`.

# Continuous Integration [![Build Status](https://travis-ci.org/mizzao/andrewmao.net.svg?branch=master)](https://travis-ci.org/mizzao/andrewmao.net)

[html-proofer] is used with Travis CI to check for broken links on new builds.

[html-proofer]: https://github.com/gjtorikian/html-proofer

# Test Manually

- `bundle exec rake`

# Update Gems

- `bundle update`
