# ngx_friendly
nginx friendly error page.

![nginx friendly error page.](./ngx_friendly.png)

## Compatibility
* Nginx
  * 1.14.x (last tested: 1.14.0)
  * 1.13.x (last tested: 1.13.6)

* Openresty
  * 1.13.x (last tested: 1.13.6.1)

Earlier versions are not tested.

## How to use
```
# patch nginx
cd nginx-1.13.6
wget -c https://raw.githubusercontent.com/taomaree/ngx_friendly/master/ngx_friendly.patch
patch -p0 < ngx_friendly.patch
./configure
make 
sudo make install


# patch openresty
wget -c https://raw.githubusercontent.com/taomaree/ngx_friendly/master/ngx_friendly.patch
wget -c https://openresty.org/download/openresty-1.13.6.1.tar.gz
tar zxf openresty-1.13.6.1.tar.gz
cd openresty-1.13.6.1/bundle/nginx-*
patch -p0 < ../../../ngx_friendly.patch
cd ../../
./configure
make 
sudo make install

```

## Contribute
Any help would be appreciated! Especially someone could turn this patch into an nginx module.

## License
ngx_friendly is [BSD licensed](./LICENSE).

## Credits
This project inspired by and forked from [Tengine](https://github.com/alibaba/tengine/blob/master/src/http/ngx_http_special_response.c).
