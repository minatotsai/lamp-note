# lamp-note
安裝LAMP以及常用指令</br>
版本ubuntu_16.04</br>

sudo apt-get install apache2</br>
安裝APACHE(2.4ver)</br>

sudo apt-get install libapache2-mod-php php-mcrypt php-mysql</br>
安裝php</br>

sudo apt-get install mysql-server</br>
安裝mysql</br>
之後會請你設置ROOT的密碼</br>
New password for the Mysql "root" user:</br>
******</br>

檢查檔案dir.conf是否有無支援.PHP檔</br>
sudo nano /etc/apache2/mods-enabled/dir.conf</br>
DirectoryIndex **index.php** index.html index.cgi index.pl index.xhtml inde$ </br>

之後重啟APACHE</br>
sudo service apache2 restart</br>

建立一個PHPINFO檔案測試是否正常
sudo nano /var/www/html/info.php</br>
`<?php`</br>
	`phpinfo();`</br>
`?>`</br>
開啟網址列輸入{自己的IP}/info.php
出現以下畫面就是成功了
![info](https://user-images.githubusercontent.com/30998953/29995268-3d3a2ce8-9018-11e7-914f-38ddb886cef1.jpg)

**常用指令**</br>
sudo service apache2 restart --重啟APACHE</br>
cd /var/log/apache2/ --移至LOG資料夾</br>
sudo nano /etc/apache2/mods-enabled/dir.conf --修改dir.conf此檔案的內容(vi 亦同)</br>
