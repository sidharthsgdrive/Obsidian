- Following [How to Install Tomcat on Fedora](https://www.atlantic.net/dedicated-server-hosting/how-to-install-tomcat-on-fedora/)
- tried making a `systemctl` service, but can't get it to work. But I think directly running `/opt/tomcat/bin/startup.sh` might do the trick.
- configuring tomcat user: 
	- in `/opt/tomcat/conf/tomcat-users.xml`, added
```XML
<role rolename="manager-gui"/>
<role rolename="manager-script"/>
<role rolename="manager-jmx"/>
<role rolename="manager-status"/>
<user username="admin" password="admin" roles="manager-gui,manager-script,manager-jmx,manager-status"/>
```
- deleted the lines mentioned in the article.
- 

****
```bash
find WEB-INF/classes/com/surveyportal -name "*.java" -print0 | \
xargs -0 javac -cp "/opt/tomcat/lib/servlet-api.jar:WEB-INF/lib/mysql-connector-j-8.0.33.jar:." -d WEB-INF/classes
```