# create-virtual-host
create virtual host within 10 minutes for Apache and Nginx 

--------------------------------------
Apache
--------------------------------------
sudo mkdir -p /var/www/example<br/>
sudo chown -R $USER:$USER /var/www/example<br/>
sudo cp /etc/apache2/sites-available/000-default.conf /etc/apache2/sites-available/example.conf<br/>
sudo nano /etc/apache2/sites-available/example.conf <br/>
sudo a2ensite example.conf<br/>
sudo systemctl restart apache2<br/>

-------------------------------------
Nginx
-------------------------------------
sudo mkdir -p /var/www/example<br/>
sudo chown -R $USER:$USER /var/www/example<br/>
sudo chmod -R 755 /var/www/example<br/>
nano /var/www/iamvipin/index.php<br/>
sudo cp /etc/nginx/sites-available/default /etc/nginx/sites-available/example<br/>
sudo nano /etc/nginx/sites-available/example<br/>
sudo ln -s /etc/nginx/sites-available/example /etc/nginx/sites-enabled/<br/>
sudo systemctl restart nginx<br/>
