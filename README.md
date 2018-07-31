SpreeDigitalAssets
==================

This gem allows you to have a central repository of the assets. The assets can be uploaded well
in advance and can be associated with the products/variants at the time of product/variant
creation.

This will also act as a central repository that can be used to access all the assets of the system
and can then be used in different products.

Demo
-----------------------------------

Try Spree Digital Assets for Spree Master with direct deployment on Heroku:

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/vinsol-spree-contrib/spree-demo-heroku/tree/spree-digital-assets-master)

Try Spree Digital Assets for Spree 3-4 with direct deployment on Heroku:

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/vinsol-spree-contrib/spree-demo-heroku/tree/spree-digital-assets)

Try Spree Digital Assets for Spree 3-1 with direct deployment on Heroku:

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/vinsol-spree-contrib/spree-demo-heroku/tree/spree-digital-assets-3-1)


## Features

* Has default folders “Documents”, “Photos” and “Graphics”

* Assets can be uploaded to each folder by using the upload feature

* Ability to view assets in List view

* Excellent UI

* Ability to remove / edit / download each asset

* Associate assets while creating product / variant

For more features or usage manual go [here](http://vinsol.com/spreecommerce-digital-asset-management).

## Installation

1. Add this extension to your Gemfile with this line:

  #### Spree >= 3.2

  ```ruby
    gem 'spree_digital_assets' , github: 'vinsol-spree-contrib/spree_digital_assets'
  ```

  #### Spree < 3.2

  ```ruby
  gem 'spree_digital_assets', github: 'vinsol-spree-contrib/spree_digital_assets', branch: 'X-X-stable'
  ```

  Also Add To your gemfile

  ```ruby
  gem 'browser', '2.0.3'
  ```

  The `branch` option is important: it must match the version of Spree you're using.
  For example, use `3-0-stable` if you're using Spree `3-0-stable` or any `3.0.x` version.

2. Install the gem using Bundler:
  ```shell
  bundle install
  ```

3. Run the installation generator
  ```shell
  bundle exec rails g spree_digital_assets:install
  ```

4. Run migrations
  ```shell
  bundle exec rake db:migrate
  ```

5. Seed data
  ```shell
  bundle exec rails g spree_digital_assets:seed
  ```

## Testing

  #### Spree >= 3.1

  For Building Dependencies:
  ```shell
  appraisal install
  ```

  The dummy app can be regenerated by using:
  ```shell
  appraisal spree-3-1 rake test_app

  ```
  This will run rake test_app using the dependencies configured for Spree 3.1. Similarly you can use spree-3-2 and spree-master for generating dummy applications using dependencies for Spree 3.2 and latest version of Spree


  ```shell
  appraisal spree-3-1 rspec
  ```
  This will run rspec using the dependencies configured for Spree 3.1. Similarly you can use spree-3-2 and spree-master to run rspec using dependencies for Spree 3.2 and latest version of Spree


  #### Spree 3.0 and Spree 2.x

  First bundle your dependencies, then run `rake`. `rake` will default to building the dummy app if it does not exist, then it will run specs. The dummy app can be regenerated by using `rake test_app`.

  ```shell
  bundle
  bundle exec rspec spec
  ```

## Contributing

1. [Fork](https://help.github.com/articles/fork-a-repo) the project
2. Make one or more well commented and clean commits to the repository. You can make a new branch here if you are modifying more than one part or feature.
3. Add tests for it. This is important so I don’t break it in a future version unintentionally.
4. Perform a [pull request](https://help.github.com/articles/using-pull-requests) in github's web interface.

## Credits

[![vinsol.com: Ruby on Rails, iOS and Android developers](http://vinsol.com/vin_logo.png "Ruby on Rails, iOS and Android developers")](http://vinsol.com)

Copyright (c) 2017 [vinsol.com](http://vinsol.com "Ruby on Rails, iOS and Android developers"), released under the New MIT License
