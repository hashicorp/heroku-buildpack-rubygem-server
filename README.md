# RubyGem Server Build Pack

This is a build pack that creates a valid RubyGem server for the
gems in the build directory, allowing you to serve your own
private RubyGems.

## Usage

Place various `.gem` files in your project root. The buildpack will find
all `.gem` files in the top-level directory and serve them.

Configure your application to use this buildpack:

```
$ heroku config:add BUILDPACK_URL=https://github.com/hashicorp/heroku-buildpack-rubygem-server.git
```

And push! Your Heroku app is now a gem server.
