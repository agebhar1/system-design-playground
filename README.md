# System Design Playground

## Build

```sh
$ vagrant up
$ ansible-playbook webservers.yml
…
$ curl 192.168.56.{2,3}
<!DOCTYPE html>
<html>
<head>
<title>Welcome to nginx!</title>
<style>
html { color-scheme: light dark; }
body { width: 35em; margin: 0 auto;
font-family: Tahoma, Verdana, Arial, sans-serif; }
</style>
</head>
<body>
<h1>Welcome to nginx!</h1>
<p>If you see this page, the nginx web server is successfully installed and
working. Further configuration is required.</p>

<p>For online documentation and support please refer to
<a href="http://nginx.org/">nginx.org</a>.<br/>
Commercial support is available at
<a href="http://nginx.com/">nginx.com</a>.</p>

<p><em>Thank you for using nginx.</em></p>
</body>
</html>
…
$ curl -H 'User-Agent: nessus' -H 'X-Request-ID: 1' 192.168.56.{2,3}
<html>
<head><title>403 Forbidden</title></head>
<body>
<center><h1>403 Forbidden</h1></center>
<hr><center>nginx/1.26.1</center>
</body>
</html>
…
```

## Links

- https://coreruleset.org/
- https://github.com/SpiderLabs/ModSecurity
- https://github.com/SpiderLabs/ModSecurity-nginx
- http://nginx.org/en/download.html
- https://www.nginx.com/blog/compiling-and-installing-modsecurity-for-open-source-nginx/
- https://www.nginx.com/blog/deploying-nginx-plus-as-an-api-gateway-part-1/
- https://www.nginx.com/resources/wiki/start/topics/examples/logrotation/
- https://www.digitalocean.com/community/tutorials/how-to-configure-logging-and-log-rotation-in-nginx-on-an-ubuntu-vps
- https://www.englert.one/logrotate-tutorial
- https://bellard.org/quickjs/
