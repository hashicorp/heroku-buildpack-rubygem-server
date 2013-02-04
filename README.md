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

## Warning!

This buildpack uses `gem server` to serve your gems. There is no authentication
or protection against someone downloading all the gems served by this gem
server as long as the URL is known.

Therefore, corporate secrets and other such private things should not be
put into this gem server unless it is behind a trusted corporate firewall.
