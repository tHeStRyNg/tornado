#### Nginx Configuration

So Node runs on port 3000 and we want to serve it at 80->443 
so to do that we use nginx with proxy-rewrite to forward the requests ffrom port 443 to 3000 internally within the app

Its configuration is within this dir for future reference.

Also we use Certbot for SSL certificates in which we use the following configuration:

``` https://certbot.eff.org/instructions?ws=nginx&os=ubuntufocal ```

#### Install Certbot
```sudo snap install --classic certbot```

#### Choose how you'd like to run Certbot
```certbot --nginx```