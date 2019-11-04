# Usage

Change the folder permission to make sure that the container is able to access the directory:
```
$ sudo chmod -R 777 addons
$ sudo chmod -R 777 etc
```

Init /etc files :
```
cp etc/odoo.conf.template etc/odoo.conf
cp etc/odoo-server.log etc/odoo.server.log 
```

Create empty acme.json for Let's Encrypt SSL/HTTPS:
```
touch acme.json
sudo chmod 600 acme.json
```

Start the container:
```
$ docker-compose up
```

* Then open `localhost:8071` to access Odoo 12.0. If you want to start the server with a different port, change **8071** to another value:

```
ports:
 - "8071:8069"
```

* Log file is printed @ **etc/odoo-server.log**

To run in detached mode, execute this command:

```
$ docker-compose up -d
```

# Custom addons

The **addons** folder contains custom addons. Just put your custom addons if you have any.

# Odoo configuration

To change Odoo configuration, edit file: **etc/odoo.conf**.

# docker-compose.yml

* odoo:12.0
* postgres:9.5

# Included Odoo Modules:
Alle Modules from https://github.com/muk-it

# Odoo 12 screenshots

![odoo-12-welcome-docker](screenshots/odoo-12-welcome-screenshot.png)

![odoo-12-apps-docker](screenshots/odoo-12-apps-screenshot.png)

![odoo-12-sales](screenshots/odoo-12-sales-screen.png)
