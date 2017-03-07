# gemstash

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
