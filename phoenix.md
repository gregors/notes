# Phoenix

## Update generator
* `mix local.phx`

## Generate a new app
* `mix phx.new --no-html --no-assets --no-gettext --binary-id`

## Generate api app
* `mix phx.new --no-html --no-assets --no-live --no-dashboard --no-gettext --no-ecto`

## set phx logger to debug
* `Logger.configure_backend(:console, level: :debug)`
