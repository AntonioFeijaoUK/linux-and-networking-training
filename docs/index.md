
# [FeijaoUK](https://feijaouk.com)

> helping beginners understanding IT Technologies

* link to training page [https://feijaouk.github.io/linux-and-networking-training/](https://feijaouk.github.io/linux-and-networking-training/)


---------------------------------------------------------------------------------

* [Linux](https://en.wikipedia.org/wiki/Linux)

> Linux is a name which broadly denotes a family of free and open-source software operating systems (OS) built around the Linux kernel


* [Networking - Networking hardware](https://en.wikipedia.org/wiki/Networking_hardware)

> Networking devices may include gateways, routers, network bridges, modems, wireless access points, networking cables, line drivers, switches, hubs, and repeaters; and may also include hybrid network devices such as multilayer switches, protocol converters, bridge routers, proxy servers, firewalls, network address translators, multiplexers, network interface controllers, wireless network interface controllers, ISDN terminal adapters and other related hardware.


* [Training and development](https://en.wikipedia.org/wiki/Training_and_development)

> Training and development can be described as "an educational process which involves the sharpening of skills, concepts, changing of attitude and gaining more knowledge to enhance the performance of employees"


---------------------------------------------------------------------------------

## Markdown basics

# This is header 1

## This is header 2

### This is header 3

* normal text

Paragraph text

	text with a <tab>

> this is a quote in markdown

## sample code in shell scripting

```bash

for NUMBER in {1..10} ; 
  do echo "Hello World $(date)" ; 
done

```


* this is a link and useful page to learn more about Markdown [https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)


---------------------------------------------------------------------------------

## Todo list and requirements

- [ ] PC/laptop

- [ ] empty pendrive 16GB minimum

- [ ] Email account

- [ ] Create account on GitHub

- [ ] Copy this list into your own page

- [ ] 

- [ ] 


## after training suggestion

- [ ] Install, explore [SoloLearn](https://www.sololearn.com/) ![SoloLeasrn](https://www.sololearn.com/Uploads/sololearn_banner.jpg)

- [ ] understand meaning of this google search ```sololearn site:sololearn.com```

- [ ] Check what is bootstrap


---------------------------------------------------------------------------------

## Training Level 1

### 1.1 - Linux Fundamentals

* Linux
  - Ubuntu
  
  - [Centos](https://www.centos.org/)
  ![Centos](https://www.centos.org/images/logo_small.png)
  
  - Fedora
  
* Windows



---------------------------------------------------------------------------------

### 1.2 - Network Fundamentals

- localhost
- 127.0.0.1

- 192.168.0.1 / 24


---------------------------------------------------------------------------------

## Sample Linux commands and useful notes

## Chrome

* Chrome links and notes, *copy/paste into the URL bar *
  - ```chrome://net-internals/#dns```    // usefull do delete chrome's dns cache
  - ```chrome://chrome-urls/```


## IT and Cyber Security

### links

* https://www.krackattacks.com/

* [https://www.wonderhowto.com/](https://www.wonderhowto.com/)


## Some usefull Linux commands and best practices

* https://stackoverflow.com/questions/4922943/test-from-shell-script-if-remote-tcp-port-is-open

```bash

  nc -z -v -w5 <host> <port>
  
  timeout 1 bash -c 'cat < /dev/null > /dev/tcp/google.com/80'
  echo $?

```

### curl

```shell
curl -k -X TRACE https://ipinfo.io/

# if is allowed, please disabled it

vim /etc/httpd/conf/httpd.conf
   TraceEnable Off
    
```


### hardenight httpd

```shell

httpd -V

Options -Indexes

ServerTokens Prod

ServerSignature Off

```

### using SSLScan

* [https://www.youtube.com/watch?v=VgaF5Ev2VW0](https://www.youtube.com/watch?v=VgaF5Ev2VW0)
* https://github.com/rbsec/sslscan

```shell

yum install sslscan

yum install git gcc openssl-devel

sslscan www.YOURSITE.com:443

sslscan https://www.YOURSITE.com:443


## check what others are using

sslscan https://www.google.com


## change httpd.config 

vim  /etc/httpd/conf.d/ssl.conf

SSLProtocol -ALL +TLSv1 +TLSv1.1 +TLSv1.2

# or

SSLProtocol all -SSLv2 -SSLv3

```


### Working with files Linux Command Linux

* [Youtube - Practical Linux Commands For Real Life](https://www.youtube.com/watch?v=08Tg1aTouMA)

```shell

ls -al !(*.txt|*.java)

# also works with rm ....


find / -xdev -type f -size +100M -exec du -sh {} ';' | sort -r | head -n 10


pkill -f httpd


yum history all

yum history info 4

yum history undo 4


makewhatis
apropos file | grep zip


yum locate */localte

yum install mlocate

updatedb
locate

localte httpd | xargs ls -la

crontab -e

ls -ls /var/spool/cron


crontab -eu root
crontab -eu ec2-user

```


### curl -vso

* curl -vso /dev/null https://feijaouk.com

```bash

curl -vso /dev/null https://feijaouk.com
* Rebuilt URL to: https://feijaouk.com/
*   Trying 192.0.78.24...
* TCP_NODELAY set
* Connected to feijaouk.com (192.0.78.24) port 443 (#0)
* TLS 1.2 connection using TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256
* Server certificate: tls.automattic.com
* Server certificate: Let's Encrypt Authority X3
* Server certificate: DST Root CA X3
> GET / HTTP/1.1
> Host: feijaouk.com
> User-Agent: curl/7.54.0
> Accept: */*
> 
< HTTP/1.1 200 OK
< Server: nginx
< Date: Wed, 29 Nov 2017 12:25:55 GMT
< Content-Type: text/html; charset=UTF-8
< Transfer-Encoding: chunked
< Connection: keep-alive
< Strict-Transport-Security: max-age=86400
< Vary: Accept-Encoding
< Vary: Cookie
< X-hacker: If you're reading this, you should visit automattic.com/jobs and apply to join the fun, mention this header.
< Link: <https://wp.me/8gh7g>; rel=shortlink
< X-ac: 3.lhr _dfw
< 
{ [945 bytes data]
* Connection #0 to host feijaouk.com left intact

```
