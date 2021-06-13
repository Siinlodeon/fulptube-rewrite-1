# FulpTube Rewrite Dockerized

make a new file named `.env` and let it have the contents of MYSQL_ROOT_PASSWORD=yourpassword

then just run `docker-compose up --build` to start up a brand new fulptube instance!!1

unfortunately, php, phpmyadmin, AND the queuer all may start before mysql finishes initializing.

i can't do much about php and phpmyadmin (the connections are done per-page so it doesn't matter anyway, the user will just have to refresh for a bit), but I have added extra handling in a new version of the queuer packaged with this dockerized version of fulptube to help with this.
