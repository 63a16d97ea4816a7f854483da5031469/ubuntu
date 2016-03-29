#mv && cp

If you use the command below, it will not replace the existing file in that folder:
sudo cp /var/tmp/xxx.war /var/lib/tomcat7/webapps/xxx.war


If you use the command below, it will replace the existing file in that folder:
sudo mv /var/tmp/xxx.war /var/lib/tomcat7/webapps/xxx.war

