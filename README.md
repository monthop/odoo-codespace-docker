# test in codespace

## test odoo 19
cd ce/19.0\
docker compose up

## test odoo 19, homesumana version

cd ce-homesumana/19.0\
docker build -t homesumana/odoo-docker:19 .\
docker compose up

## test odoo 19 Enterprise, homesumana version

cd ee-homesumana/ee-src\
tar -xvzf ../../ee/wattana_psnsoft/odoo_19.0+e.latest.tar.gz

cd ee-homesumana/19.0\
docker build -t homesumana/odoo-docker:19 .\
docker compose up
