# Ghost CMS Nginx and Host Configuration

Ghost CMS Nginx, Host and SSL Configuration

### example.com.conf

```sh

sudo nano /var/www/ghost/system/files/example.com.conf

```

### example.com-ssl.conf

```sh

sudo nano /var/www/ghost/system/files/example.com-ssl.conf

```

### ssl-params.conf

```sh

sudo nano /var/www/ghost/system/files/ssl-params.conf

```

<p>These files generate and Configure while installing Ghost via Ghost-CLI</p>
<p>I add extra functions on the Nginx and Host configuration file</p>

### Force SSL redirect

File  - example.com.conf

```
# Redirect HTTP to HTTPS - Remove this if you are Not Configuring SSL for your Ghost Blog
    if ($scheme = http) {
        return 301 https://$server_name$request_uri;
    }
    
 ```

### Remove Powered by HTTP header

Files - example.com.conf and  example.com-ssl.conf

```
 proxy_hide_header X-powered-by;
 ```

### Remove x-xss-protection
 
File - ssl-params.conf

```
add_header x-xss-protection "1; mode=block" always;
```

### Features


- Secure SSL A+ Grade
- Force SSL
- Nginx Proxy
- Hide Powered by

### Latest and Updated Files

- example.com.conf
- example.com-ssl.conf
- ssl-params.conf

### Deprecated Files

- <strike>ghost.conf</strike>
- <strike>ghost.service</strike>


<p>Fork this github repository.Every Month we will update this Respository After Configuration test</p>

<p>Maintained by Santhosh veer</p>

Here is Full Installation Guide to Install Ghost Blog CMS on Ubuntu with Free SSL and HTTP/2 - <a href="https://itrendbuzz.com/install-ghost-cli-on-digitalocean/">Read Now</a>

(C) 2017 itrendbuzz.com


