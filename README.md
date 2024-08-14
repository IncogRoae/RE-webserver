## Nginx Web Server

Documentation is available at http://nginx.org

### 빌드

`configure`와 `make`를 이용해 컴파일 합니다.

**컴파일 옵션**
```
--prefix=/etc/nginx \
--sbin-path=/usr/sbin/nginx \
--conf-path=/etc/nginx/nginx.conf \
--error-log-path=/var/log/nginx/error.log \
--http-log-path=/var/log/nginx/access.log \
--pid-path=/var/run/nginx.pid \
--lock-path=/var/run/nginx.lock \
--with-http_ssl_module \
--with-http_v2_module \
--with-http_gzip_static_module
```

> **Note**
>
> OpenSSL 3 버전대를 사용하면서 deprecated되는 항목들이 있어 컴파일 에러가 발생합니다.
> 따라서 임시적으로 CFLAGS="-Wno-deprecated-declarations"를 추가하여 컴파일을 진행합니다.
