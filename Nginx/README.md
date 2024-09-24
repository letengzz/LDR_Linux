# Nginx

Nginx服务器1、Nginx 是一个高性能的web服务器；（服务器）2、Nginx 是俄罗斯人Igor Sysoev用C语言开发的，第一个版本0.1.0发布于2004年10月4日；商业版本：http://www.nginx.com开源版：http://nginx.org 下载：wget http://nginx.org/download/nginx-1.24.0.tar.gz

Nginx启动

1、启动nginx执行命令：/usr/local/nginx/sbin/nginx -c /usr/local/nginx/conf/nginx.conf（其中-c是指定配置文件）

2、检查Nginx是否启动：通过查看进程：ps -ef | grep nginxNginx重启/usr/local/nginx/sbin/nginx -s reload

分布式集群部署Nginx服务器Nginx关闭1、优雅关闭Nginx：找出nginx的进程号：ps -ef | grep nginx执行命令：kill -QUIT 主pid       kill -QUIT 4702其中pid是主进程号的pid（master process），其他为子进程pid（worker process）优雅关闭会将已经进来的请求处理完后再关闭；2、快速关闭Nginx：找出nginx的进程号：ps -ef | grep nginxkill -TERM 主pid快速关闭会直接关闭，已经进来的请求也不会处理；(暴力方式)

分布式集群部署Nginx服务器Nginx配置检查conf/nginx.conf当修改Nginx配置文件后，可以使用Nginx命令进行配置文件语法检查，用于检查Nginx配置文件是否正确；检查Nginx配置文件是否正确：/usr/local/nginx/sbin/nginx -c /usr/local/nginx/conf/nginx.conf -t

Nginx服务器Nginx负载均衡1、在http模块配置upstream：upstream api {      	server  192.168.11.128:9000;       	server  192.168.11.129:9000;       	server  192.168.11.130:9000;        	server  192.168.11.131:9000;  } 2、在server模块里配置：location / {	proxy_pass http://api;}

upstream webui {      	server  192.168.11.128:9001;       	server  192.168.11.129:9001;       	server  192.168.11.130:9001;        	server  192.168.11.131:9001;  } 

location /webui {	proxy_pass http://webui;}



location / {                 proxy_set_header Host $http_host;                 proxy_set_header Server MinIO;                 proxy_set_header Accept-Ranges bytes;	proxy_pass http://api;}