### Installation of Web Server

> Step 1: Check httpd software using # rpm -q httpd, if it's not present. then run the following cmd to install httpd

```
# yum install httpd -y
```
> Step 2: Go inside /var/www/html file using following cmd.
```
# cd /var/www/html
```
> Step 3: Make a html file using any editor, but here, I am using vim editor. so you can install to use the following cmd.
```
# yum install vim -y
```

> ***Note*** : Here, I am making a "test.html" file to test the congfigure. 
```
Hello, this is my test html file.
```
> Step 4: Check your the status of httpd service is active or not.
```
[root@ip-172-31-44-11 html]# systemctl status httpd
● httpd.service - The Apache HTTP Server
   Loaded: loaded (/usr/lib/systemd/system/httpd.service; disabled; vendor preset: disabled)
   Active: inactive (dead)
     Docs: man:httpd.service(8)

```


> Step 5: Do Active your service.
```
# systemctl start httpd
```
> ***Note*** Now you can check your httpd service again using same cmd and you will see, now your service is in active mode.
```
# systemctl status httpd
```
```
[root@ip-172-31-44-11 html]# systemctl status httpd
● httpd.service - The Apache HTTP Server
   Loaded: loaded (/usr/lib/systemd/system/httpd.service; disabled; vendor preset: disabled)
   Active: active (running) since Thu 2020-09-24 06:13:53 UTC; 6min ago
     Docs: man:httpd.service(8)
 Main PID: 13356 (httpd)
   Status: "Running, listening on: port 80"
    Tasks: 213 (limit: 4936)
   Memory: 24.9M
   CGroup: /system.slice/httpd.service
           ├─13356 /usr/sbin/httpd -DFOREGROUND
           ├─13357 /usr/sbin/httpd -DFOREGROUND
           ├─13358 /usr/sbin/httpd -DFOREGROUND
           ├─13359 /usr/sbin/httpd -DFOREGROUND
           └─13360 /usr/sbin/httpd -DFOREGROUND
```
> ***Note*** : Here, I am disable firewalld service it has lots of reason.
```
#systemc



