# About
This is simply a lmgtfy.com remake without ads. This was forked from Arinerron/re-lmgtfy with very few changes.

# How do I use it?
Visit https://lmgtfy.wtf/ and type in the info it asks for to generate a lmgtfy.wtf link.

# To build for yourself.
- Modify the url in index.html
- Generate your certificates with nginx.
- Modify the nginx.conf file for your custom domain.
- Copy index.html and go.html into your www folder. `cp re-lmgtfy/index.html www/index.html`
- Run the nginx docker command.

```bash
docker run -d -p 80:80 -p 443:443 -v /etc/letsencrypt/live/lmgtfy.wtf/:/certs/ -v /root/re-lmgtfy/html/:/www/ -v /root/re-lmgtfy/nginx.conf:/etc/nginx/nginx.conf nginx
```