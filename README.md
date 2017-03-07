# gemstash[![](https://images.microbadger.com/badges/version/jorgeandrada/gemstash:master.svg)](https://microbadger.com/images/jorgeandrada/gemstash:master "Get your own version badge on microbadger.com") [![](https://images.microbadger.com/badges/image/jorgeandrada/gemstash:master.svg)](https://microbadger.com/images/jorgeandrada/gemstash:master "Get your own image badge on microbadger.com") [![](https://images.microbadger.com/badges/commit/jorgeandrada/gemstash:master.svg)](https://microbadger.com/images/jorgeandrada/gemstash:master "Get your own commit badge on microbadger.com")

## Despliegue del servidor:

```
mkdir /srv/gemstash
docker run -d --name gemstash \
  -v /srv/gemstash:/root/.gemstash \
  -p 9292:9292 \
  jorgeandrada/gemstash:latest
```

## Configuración en clientes:
```ruby
bundle config mirror.https://rubygems.org http://DOMINIOPROXYCACHE:9292
bundle config mirror.https://rubygems.org.fallback_timeout true
bundle config mirror.https://rubygems.org.fallback_timeout 30
```

Información: https://github.com/bundler/gemstash
