# docker-laravel-example
# This repo is for deploying PHP, MYSQL and Laravel via docker.
# Bu repo PHP, MYSQL ve Laraveli docker üzerinden ayağa kaldırmak içindir.



#ENGLISH
- Run "docker compose up -d from terminal" in the main directory of the file.
- After the containers are installed, open a terminal in PHP container from docker desktop and run "composer create-project laravel/laravel ." command.
- After that, the laravel project will be installed on docker.
- It will give an error because it does not have some file permissions and sqlite permission. Run the following commands in order.


1. chown -R www/data:www-data/var/www/html/storage var/www/html/bootstrap/cache
2. chown www-data:www-data database/database.sqlite
   **After these operations, laravel will stand up on docker and you will be able to see the laravel home screen at http://localhost:8012/**


**MYADMIN IS NOT INSTALLED IN THE PROJECT, YOU CAN CONNECT WITH A REMOTE CONNECTOR (HEIDISQL, Sequel PRO)**

##############################################################################################

#TURKISH
- Dosyanın ana dizininde "terminalden docker compose up -d" komutunu çalıştır.
- Containerlar kurulduktan sonra docker desktoptan PHP containerında terminal aç ve "composer create-project laravel/laravel ." komutunu çalıştır.
- İşlemler bittikten sonra laravel projesi docker'a kurulmuş olacak.
- Bazı dosya izinleri ve sqlite izni olmadığı için hata verecektir. Sırasıyla aşağıdaki komutları çalıştır.

    1. chown -R www/data:www-data/var/www/html/storage var/www/html/bootstrap/cache
    2. chown www-data:www-data database/database.sqlite

**Bu işlemlerden sonra laravel docker üzerinden ayağa kalkacaktır ve http://localhost:8012/ adresinde laravel giriş ekranını görebileceksin.**

**PROJEDE MYADMIN KURULU DEĞİLDİR UZAK BAĞLANTI ARACIYLA BAĞLANABİLRSİN. (HEIDISQL, Sequel PRO)**
