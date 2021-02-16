# Nginx with TLS1.3, HTTP/1 & HTTPS

- Nginx can act both as a web server and a proxy
- cd .etc/nginx
- Delete the content the existing nginx.conf file and write one from scratch

### To make nginx a static web server

#### Serving a single directory

- use the root directive to specify path to content to server
- Running nginx with: nginx; would result in an error because nginx runs on port 80, by default
- To stop default running nginx, run: nginx -s stop
- Then run: nginx
- Open the IP address specified in nginx.conf to find web content being served.

#### Serving directories with relative paths

- Add/ Create directories
- cd /etc/nginx.conf and run: nginx -s reload
- Visit each directory using: /directory-name; to serve their content

#### Serving content from an outside directory

- Use the "location" directive to specify path to the directory
- Run: nginx -s reload
- Visit browser and specify path to the outside directory. The server should return a 403 error
- Specifying the full path however, would serve the content in the directory (i.e adding the filename with its extension)

#### Restricting access with the "location" directive and regex

- location ~ <regex-goes-here>; next specify a return response
