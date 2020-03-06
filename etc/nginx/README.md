## nginx

nginx.conf with SSL forward secrecy enabled

### Use this command to generate `dhparam.pem`

    openssl dhparam -out dhparam.pem 2048

### How to use RTMP in nginx

Load module

    load_module lib64/nginx/modules/ngx_rtmp_module.so;

```
rtmp_auto_push on;

rtmp {
    server {
        listen 1935;

        application live {
            live on;
        }
    }
}
```
