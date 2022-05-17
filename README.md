# LEMP-STACK-PROJ2

step 4
 Telling nginx to use our php processor
 now to check if there is any error with your configurated file
```
sudo nginx -t
```

Now we need to disable default nginx host that is currently configured to run on port 80 before we run our application

```
sudo unlink /etc/nginx/sites-enabled/default

```

Now we need to reload nginx by using 

```
  sudo systemctl reload nginx
```

Now we have a new website but our web root  is emtpty(/var/www/projectLEMP). we need to create an index file in that same directory so that we can test our block server

```
sudo echo 'Hello LEMP from hostname' $(curl -s http://169.254.169.254/latest/meta-data/public-hostname) 
'with public IP' $(curl -s http://169.254.169.254/latest/meta-data/public-ipv4) > /var/www/projectLEMP/index.html
```
