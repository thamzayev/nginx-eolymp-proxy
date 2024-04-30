# Forward Proxy Server

This is a Dockerfile with nginx server built with the [ngx\_http\_proxy\_connect\_module](https://github.com/chobits/ngx_http_proxy_connect_module) which blocks all outgoing traffic.

# E-Olymp

Main purpose of this repository to disable access to websites while e-olymp programming olympiad platform is allowed.

## Build and Run

```
git clone https://github.com/thamzayev/nginx-eolymp-proxy.git
cd nginx-eolymp-proxy
docker build -t nginx-eolymp-proxy .
```

To disable access to other websites except E-Olymp use the code below:

```
docker run -d -p 8888:8888 -v ./eolymp_allowlist.conf:/usr/local/nginx/conf/nginx.conf nginx-eolymp-proxy
```

or

```
docker-compose up -d
```