# create-virtual-host
create virtual host within 10 minutes for Apache and Nginx 

--------------------------------------
Apache
--------------------------------------
sudo mkdir -p /var/www/iamvipin
sudo chown -R $USER:$USER /var/www/iamvipin
sudo cp /etc/apache2/sites-available/000-default.conf /etc/apache2/sites-available/iamvipin.conf
sudo nano /etc/apache2/sites-available/iamvipin.conf 
sudo a2ensite iamvipin.conf
sudo systemctl restart apache2

-------------------------------------
Nginx
-------------------------------------
sudo mkdir -p /var/www/iamvipin
sudo chown -R $USER:$USER /var/www/iamvipin
sudo chmod -R 755 /var/www/iamvipin
nano /var/www/iamvipin/index.php
sudo cp /etc/nginx/sites-available/default /etc/nginx/sites-available/iamvipin
sudo nano /etc/nginx/sites-available/iamvipin
sudo ln -s /etc/nginx/sites-available/iamvipin /etc/nginx/sites-enabled/
sudo systemctl restart nginx
