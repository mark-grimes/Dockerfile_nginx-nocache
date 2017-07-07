# nginx-nocache

A simple variation on the official nginx image that turns off caching by setting `sendfile` to `off`. Useful for web development where you want to be constantly changing files and immediately seeing the new results.

## Licence

Whatever the official nginx image is. Do what you like with the changes I've made.

## Usage

Run with your content directory mapped to `/usr/share/nginx/html`, and a port mapped to port 80 in the container. For example:

```
docker run --name nginx -v /path/to/my/content:/usr/share/nginx/html:ro -d -p 8080:80 markgrimes/nginx-nocache
```

Then direct your browser to `http://localhost:8080/`.  If you're using docker-machine on Mac or Windows then you need to use the VMs IP address instead of `localhost`.

For more information see [the official image](https://hub.docker.com/_/nginx/).  If you're changing the config in the container (`/etc/nginx/nginx.conf`) then you might as well just use the official image instead of this one.

## Links

[Page on Docker hub](https://hub.docker.com/r/markgrimes/nginx-nocache)

[Repository on GitHub](https://github.com/mark-grimes/Dockerfile_nginx-nocache)
