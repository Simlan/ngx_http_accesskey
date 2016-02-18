Starting from NGINX 1.9.11, you can also compile this module as a dynamic module, by using the `--add-dynamic-module=PATH` option instead of `--add-module=PATH` on the
`./configure` command line above. And then you can explicitly load the module in your `nginx.conf` via the [load_module](http://nginx.org/en/docs/ngx_core_module.html#load_module)
directive, for example,

./configure  --add-dynamic-module=/home/software/nginx-accesskey-2.0.3


```nginx
load_module modules/ngx_http_accesskey_module.so;



