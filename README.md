# ngx_friendly
nginx friendly error page.

## Compatibility
* Nginx
  * 1.14.x (last tested: 1.14.0)
  * 1.13.x (last tested: 1.13.6)

Earlier versions is not tested.

## how to use
```
cd nginx-1.13.6
patch -p0 < ngx_friendly.patch
./configure
make 
sudo make install
```
