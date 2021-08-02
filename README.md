# About
This is simply a lmgtfy.com remake without ads. This was forked from Arinerron/re-lmgtfy with very few changes.

# How do I use it?
Visit https://lmgtfy.wtf/ and type in the info it asks for to generate a lmgtfy.wtf link.

# To build for yourself.
- Modify the url in index.html
- Generate your certificates with nginx. Copy to /root/certs/.
- Modify the nginx.conf file for your custom domain.
- Run the nginx docker command.

```bash
docker run -d --name nginx -p 80:80 -p 443:443 -v /root/certs/:/certs/ -v /root/re-lmgtfy/html/:/www/ -v /root/re-lmgtfy/nginx.conf:/etc/nginx/nginx.conf nginx
```