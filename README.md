[![Release](https://img.shields.io/github/release/giterlizzi/perl-Mojolicious-Plugin-Badge.svg)](https://github.com/giterlizzi/perl-Mojolicious-Plugin-Badge/releases) [![Actions Status](https://github.com/giterlizzi/perl-Mojolicious-Plugin-Badge/workflows/linux/badge.svg)](https://github.com/giterlizzi/perl-Mojolicious-Plugin-Badge/actions) [![License](https://img.shields.io/github/license/giterlizzi/perl-Mojolicious-Plugin-Badge.svg)](https://github.com/giterlizzi/perl-Mojolicious-Plugin-Badge) [![Starts](https://img.shields.io/github/stars/giterlizzi/perl-Mojolicious-Plugin-Badge.svg)](https://github.com/giterlizzi/perl-Mojolicious-Plugin-Badge) [![Forks](https://img.shields.io/github/forks/giterlizzi/perl-Mojolicious-Plugin-Badge.svg)](https://github.com/giterlizzi/perl-Mojolicious-Plugin-Badge) [![Issues](https://img.shields.io/github/issues/giterlizzi/perl-Mojolicious-Plugin-Badge.svg)](https://github.com/giterlizzi/perl-Mojolicious-Plugin-Badge/issues) [![Coverage Status](https://coveralls.io/repos/github/giterlizzi/perl-Mojolicious-Plugin-Badge/badge.svg)](https://coveralls.io/github/giterlizzi/perl-Mojolicious-Plugin-Badge)

# Mojolicious::Plugin::Badge - Badge plugin for Mojolicious

Mojolicious::Plugin::Badge is a Mojolicious plugin that generate "Shields.io"
like badge from `badge` helper or via API URL (e.g. `badge/Hello-Mojo!-orange`).

## Usage

```.pl
# Mojolicious
$self->plugin('Badge');

# Mojolicious::Lite
plugin 'Badge';

get '/my-cool-badge' => sub ($c) {

my $badge = $c->app->badge(
  label        => 'Hello',
  message      => 'Mojo!',
  color        => 'orange'
  logo         => 'https://docs.mojolicious.org/mojo/logo.png'
  badge_format => 'png',
);

$c->render(text => $badge, format => 'png');

};
```
![Hello Mojo](https://raw.github.com/giterlizzi/perl-Mojolicious-Plugin-Badge/main/examples/hello-mojo.png)


## Installation

To install this module type the following:

    perl Makefile.PL
    make
    make test
    make install

Using App::cpanminus:

    cpanm Mojolicious::Plugin::Badge


## Documentation

 - `perldoc Mojolicious::Plugin::Badge`
 - https://metacpan.org/release/Mojolicious-Plugin-Badge

## Copyright

Copyright (C) 2024 by Giuseppe Di Terlizzi
