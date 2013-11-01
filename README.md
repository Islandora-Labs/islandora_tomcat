SUMMARY
-------

This module is intended to make it easier to deploy a development
environment of islandora, by packaging up a tomcat with everything
needed. This repo is currenly being constructed and only contains
fedora, gsearch and solr. In the future more will be added.

INSTALLATION
------------

We assume there is a mysql database running on localhost. Fedora will
try to use a database named: fedora. Connecting with a username/password
of fedora/fedora. This needs to be setup before running tomcat.

To start the process you need to:
* setup mysql
* git clone git://github.com/jonathangreen/islandora_tomcat.git
* cd islandora_tomcat
* export CATALINA_HOME='.'
* export JAVA_OPTS="-Xms1024m -Xmx1024m -XX:MaxPermSize=512m -XX:+CMSClassUnloadingEnabled -Djavax.net.ssl.trustStore=$CATALINA_HOME/fedora/server/truststore -Djavax.net.ssl.trustStorePassword=tomcat"
* ./bin/startup.sh

Fedora will be running on port 8080. The fedora username and password
will be fedoraAdmin/fedoraAdmin.

TODO
----

* add djatoka
