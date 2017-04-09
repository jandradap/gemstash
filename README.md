# gemstash[![](https://images.microbadger.com/badges/version/jorgeandrada/gemstash:latest.svg)](https://microbadger.com/images/jorgeandrada/gemstash:latest "Get your own version badge on microbadger.com") [![](https://images.microbadger.com/badges/image/jorgeandrada/gemstash:latest.svg)](https://microbadger.com/images/jorgeandrada/gemstash:latest "Get your own image badge on microbadger.com") [![](https://images.microbadger.com/badges/commit/jorgeandrada/gemstash:latest.svg)](https://microbadger.com/images/jorgeandrada/gemstash:latest "Get your own commit badge on microbadger.com")

<a href='https://ko-fi.com/A417UXC' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://az743702.vo.msecnd.net/cdn/kofi2.png?v=0' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>


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
