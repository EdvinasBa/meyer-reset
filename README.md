# Eric Meyer - CSS Reset Stylesheet

Eric Meyer's CSS reset stylesheet as [Sass](http://sass-lang.com/), delivered as a [Compass Extension](http://compass-style.org/docs/tutorials/extensions/) and [Ruby Gem](http://rubygems.org/).

For more information: [http://meyerweb.com/eric/tools/css/reset/](http://meyerweb.com/eric/tools/css/reset/)

## Installation and Usage

### Compass Extension

To install as a Ruby Gem to use this as a Compass Extension, run the following in your Terminal app.

    gem install meyer-reset

Then add `require 'meyer-reset'` to your Compass config file.

Using this in your Sass stylesheet is pretty easy. Simply import the extension into your stylesheet (preferably as the first import or declaration in your Sass stylesheet).

If you look at [the extension](https://github.com/adamstac/meyer-reset/blob/master/stylesheets/_meyer-reset.sass), you will notice that we are "including" the mixin `+meyer-reset` for you in the last line. All you will need to do is import and go.

    @import meyer-reset
    
    ...

### Simple Sass Partial

For non Compass users, or someone who just wants to use this as a simple Sass partial vs installing as a Ruby Gem and Compass extension. In your terminal app, navigate to where you want to download this to.

For example: `cd path/to/project/sass`

Then use curl to pull down the raw file.

    curl -0 https://github.com/adamstac/meyer-reset/raw/master/stylesheets/_meyer-reset.sass

The same rules apply as mentioned above. All you will need to do is import and go.

    @import meyer-reset
    
    ...

### Vanilla CSS

This part of the project was included to just show how much can be done with using Sass as the pre-processor to CSS. As you can see below as well as in the "For Fun" section we can use our Sass code to output our CSS in many ways and do lots of creative things automatically with tools like [Rake](http://en.wikipedia.org/wiki/Rake_(software\)).

If you want to just use the vanilla CSS that this Sass would output check out:

* [stylesheets/compiled/meyer-reset.css](https://github.com/adamstac/meyer-reset/blob/master/stylesheets/compiled/meyer-reset.css)
* [stylesheets/compiled/meyer-reset-compressed.css](https://github.com/adamstac/meyer-reset/blob/master/stylesheets/compiled/meyer-reset-compressed.css)

Again, using curl, you can pull down either of those as raw files and just use the CSS.

    curl -0 https://github.com/adamstac/meyer-reset/raw/master/stylesheets/compiled/meyer-reset.css

    curl -0 https://github.com/adamstac/meyer-reset/raw/master/stylesheets/compiled/meyer-reset-compiled.css
    
To see how these CSS files were created, check out the section below which describes [the various Rake tasks](https://github.com/adamstac/meyer-reset/blob/master/Rakefile) included in this project.

## For fun

For those who want to learn about how to use Rake and want to play with how Sass and Compass work when compiling, run the command `rake -T` to see a list of rake tasks that: clear, build and release this gem, and compile and convert Sass.

Dig into the [Rakefile](https://github.com/adamstac/meyer-reset/blob/master/Rakefile) to see what makes all this happen.

    rake css:clear     # Clear the styles
    rake gem:build     # Build the gem
    rake gem:release   # Build and release the gem
    rake sass:compile  # Compile new styles
    rake sass:convert  # Converts the Sass to SCSS

## License

None (public domain)

* v2.0 | 20110126
* [http://meyerweb.com/eric/tools/css/reset/](http://meyerweb.com/eric/tools/css/reset/)