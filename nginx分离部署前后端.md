# mac下安装nginx

```
从nginx官方网站下载源包
wget http://nginx.org/download/nginx-1.13.4.tar.gz
tar xvzf nginx-1.13.4.tar.gz
cd nginx-1.13.4
sudo ./configure --prefix=/usr/local/nginx --with-cc-opt="-Wno-deprecated-declarations"
sudo make
sudo make install
```

# 编译好后，启动nginx

```
任意路径下
mkdir nginx         -- 用于存放项目
cp -r dist nginx    -- 把前端编译好的源码放到nginx
mv dist hmtl

拷贝conf目录到项目中去
cp -r /usr/local/nginx/conf nginx

启动：
sudo /usr/local/nginx/sbin/nginx -p /Users/chenwj/work/lytb/vue-demo/nginx -c conf/nginx.conf

-- -p 表示nginx项目的路径，nginx.conf中路径默认为-p/xxx; 比如： root html; 实际是 $-p/html;

停止:
sudo /usr/local/nginx/sbin/nginx -p /Users/chenwj/work/lytb/vue-demo/nginx -s stop
```

# 前后端分离，没有跨域问题编写

```
思路：让nginx承载所有静态请求,在nginx.conf 中

http {
	#负载均衡
	upstream javabody.org{
		server 127.0.0.1:8080 weight=1;
		server 127.0.0.1:8081 weight=2;
	}

	server{
		listen 80;
		server_name www.xxx.com;

		#所有请求都会被转发
		location / {
			#proxy_pass www.baidu.com;
			proxy_pass http://javabody.org;
			proxy_redirect default;
		}

		#静态文件保持nginx请求(这里优先级比较高)
		location ~ .*\.(js|css|ico|png|jpg|eot|svg|ttf|woff|html) {
			#所有静态文件直接读取硬盘
			root html;
			expires 30d; #缓存30天
		}
	}
}


















```