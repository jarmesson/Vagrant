server {
        listen   80 default;
        server_name  localhost;
        root   /var/www/html/sample.com;
        index index.php;
        access_log  /var/log/nginx/localhost.access.log;
        
        location / {
                try_files $uri $uri/ /index.php?$args;
        }
        
        location ~ \.php$ {
                include snippets/fastcgi-php.conf;
                fastcgi_pass unix:/run/php/php7.2-fpm.sock;
        }
        
        location ~* \.(js|css|png|jpg|jpeg|gif|ico|svg)$ {
                expires max;
                log_not_found off;
        }
}


server {
        listen   443 default;
        server_name  localhost;
        root   /var/www/html/sample.com;
        index index.php;
        access_log  /var/log/nginx/localhost.access.log;
        
        location / {
                try_files $uri $uri/ /index.php?$args;
        }
        
        location ~ \.php$ {
                include snippets/fastcgi-php.conf;
                fastcgi_pass unix:/run/php/php7.2-fpm.sock;
        }
        
        location ~* \.(js|css|png|jpg|jpeg|gif|ico|svg)$ {
                expires max;
                log_not_found off;
        }
}
