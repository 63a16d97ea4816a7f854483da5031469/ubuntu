#mv && cp

If you use the command below, it will not replace the existing file in that folder:
sudo cp /var/tmp/xxx.war /var/lib/tomcat7/webapps/xxx.war


If you use the command below, it will replace the existing file in that folder:
sudo mv /var/tmp/xxx.war /var/lib/tomcat7/webapps/xxx.war

===> This one will not Override the existing file---will not ask your decision:
sudo cp -rf /var/tmp/xxx.war /var/lib/tomcat7/webapps/xxx.war


===> This one will not Override the existing file---will ask your decision:
sudo cp -i /var/tmp/xxx.war /var/lib/tomcat7/webapps/xxx.war
