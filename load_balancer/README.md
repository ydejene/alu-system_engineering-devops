# Load Balancer Project

High-availability web stack with:
- 2 Nginx web servers (`web-01`, `web-02`)
- HAProxy load balancer (`lb-01`) in round-robin
- Custom `X-Served-By` header for tracing

## Scripts

- `0-custom_http_response_header`: Configures Nginx with `X-Served-By`
- `1-install_load_balancer`: Installs and configures HAProxy

## Test

```bash
curl -sI http://3.84.45.232 | grep X-Served-By