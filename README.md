# linux-server-configuration
Udacity FSND server configuration project

* IP address: 172.104.42.46
* SSH port: 2200
* URL: li1622-46.members.linode.com

### Summary of software and configuration
1. Access
    * Added separate users with sudo permissions
    * Change SSH port to 2200
    * Set up SSH keys for each user in /home/[user]/.ssh/authorized_keys
    * Disallow root login and password authentication
2. Firewall
    * Installed ufw
    * Default deny incoming/allow outgoing
    * Allow ports 2200, 80 and 123
3. Server
    * Installed Apache
    * Installed the WSGI module to hand off to the Python application
4. Database
    * Installed PostgreSQL    
    * Remote connections are disallowed by default
    * Created a user and a database for the application
5. Setting up catalog application
    * Installed Git
    * Cloned the application into /srv/www/flask_category    
    * Installed dependencies:
        * Flask
        * SQLAlchemy
        * httplib2
        * requests
        * oauth2client
    * Installed psycopg2 to connect to PostgreSQL
    * Updated permissions so Apache can access the application folders

### Third-party resources used
* https://www.linode.com/docs/getting-started/
* https://www.digitalocean.com/community/tutorials/how-to-create-a-sudo-user-on-ubuntu-quickstart
* https://www.ssh.com/ssh/putty/windows/
* https://nz.godaddy.com/help/changing-the-ssh-port-for-your-linux-server-7306
* https://www.linode.com/docs/security/securing-your-server/#configure-a-firewall
* https://www.linode.com/docs/security/firewalls/configure-firewall-with-ufw/
* https://www.digitalocean.com/community/tutorials/how-to-secure-postgresql-on-an-ubuntu-vps
* https://www.postgresql.org/docs/8.0/user-manag.html
* https://docs.sqlalchemy.org/en/latest/core/engines.html#postgresql
* https://superuser.com/questions/635289/what-is-the-recommended-directory-to-store-website-content
* https://modwsgi.readthedocs.io/en/develop/configuration-directives/WSGIScriptAlias.html
* https://www.loggly.com/ultimate-guide/apache-logging-basics/
* https://stackoverflow.com/questions/32722143/flask-application-traceback-doesnt-show-up-in-server-log
