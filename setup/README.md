# Setup script for Redash with Docker on Ubuntu 18.04.

```
$ cp redash-dc.service /etc/systemd/services/redash-dc.service
$ systemctl enable reshash-dc && systemctl start redash-dc
$ systemctl status reshash-dc

# Setup proxy:
# before this, add A record for builder.fidap.co in Google Domains.
$ cp redash.nginx.conf /etc/nginx/sites-available/builder.fidap.co
$ ln -s /etc/nginx/sites-available/builder.fidap.co /etc/nginx/sites-enabled/builder.fidap.co
$ nginx -t && nginx -s reload
```

Official Redash Setup @ [https://github.com/getredash/setup](https://github.com/getredash/setup)
