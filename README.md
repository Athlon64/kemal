
[![Kemal](media/header.png)](http://kemalcr.com)

> Lightning Fast, Super Simple web framework.

[![Build Status](https://travis-ci.org/kemalcr/kemal.svg?branch=master)](https://travis-ci.org/kemalcr/kemal)
[![Join the chat at https://gitter.im/sdogruyol/kemal](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/sdogruyol/kemal?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

# Super Simple ⚡️

```ruby
require "kemal"

# Matches GET "http://host:port/"
get "/" do
  "Hello World!"
end

# Creates a WebSocket handler.
# Matches "ws://host:port/socket"
ws "/socket" do |socket|
  socket.send "Hello from Kemal!"
end

Kemal.run
```

Start your application!

```
crystal src/kemal_sample.cr
```
Go to *http://localhost:3000*

Check [documentation](http://kemalcr.com) or [samples](https://github.com/kemalcr/kemal/tree/master/samples) for more.

# Super Fast 🚀

Numbers speak louder than words.

| Framework             | Request Per Second  | Avg. Response Time |
| --------------------- | :-----------------: | -----------------: |
| Kemal (Production)    | 100238              |           395.44μs |
| Sinatra (Thin)        | 2274                |            43.82ms |


These results were achieved with ```wrk``` on a Macbook Pro Late 2013. (**2Ghz i7 8GB Ram OS X Yosemite**)

# Installation

Add this to your application's `shard.yml`:

```yaml
dependencies:
  kemal:
    github: kemalcr/kemal
    branch: master
```

# Features

- Support all REST verbs
- Websocket support
- Request/Response context, easy parameter handling
- Middlewares
- Built-in JSON support
- Built-in static file serving
- Built-in view templating via [Kilt](https://github.com/jeromegn/kilt)

# Documentation

You can read the documentation at the official site [kemalcr.com](http://kemalcr.com)

## Thanks

Thanks to Manas for their awesome work on [Frank](https://github.com/manastech/frank).
