# Docker-JBoss-Load-Balancer
Docker Stack for Load Balacing (testing)

## Your Application might need the 'distributable' tag in "WEB-INF/web.xml"

	<web-app xmlns=.....>
	
	   <distributable/>
	   ...
   
	   
## And also a "WEB-INF/jboss-web.xml" (...i dont know so far!) with something like this:

		<jboss-web xmlns="http://www.jboss.com/xml/ns/javaee"
	           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	           xsi:schemaLocation="http://www.jboss.com/xml/ns/javaee http://www.jboss.org/j2ee/schema/jboss-web_10_0.xsd">
	   <replication-config>
	      <replication-granularity>SESSION</replication-granularity>
	   </replication-config>
		</jboss-web>
		
##		