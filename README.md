# lamp

Run a local LAMP stack using Docker Compose to use as a 
development environment for the TokenBB Wordpress plugin.

`npm start` 

Apache will listen at `localhost:8000`. 

Make sure to add a `.env` file in `packages/docker-lamp`.  
You can find an example in [`sample.env`](sample.env)

## How to copy the data from a remote Wordpress site

1. copy `sample.env` to `.env`
2. use the duplicator plugin on the remote install to generate a "package"
3. download the "package" file (zip) and the installer (php)
4. make sure `__data/apache` exists
5. copy the package file and the installer there
6. run `docker-compose up`
7. navigate to http://localhost:8000/installer.php
8. follow the instructions
