# Nginx with TLS1.3, HTTP/1 & HTTPS

- Nginx can act both as a web server and a proxy
- cd .etc/nginx
- Delete the content the existing nginx.conf file and write one from scratch

### To make nginx a static web server

- use the root directive to specify path to content to server
- Running nginx with: nginx; would result in an error because nginx runs on port 80, by default
- To stop default running nginx, run: nginx -s stop
- Then run: nginx
- Open the IP address specified in nginx.conf to find web content being served.
