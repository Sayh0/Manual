오늘 배운 것

세션session 객체.
jsp와 servlet 분할

톰캣 설치 경로 : C:\acorn202206\apache-tomcat-8.5.81
수정할 것 
1. server.xml 의 source 중 
<Connector connectionTimeout="20000" port="8888" protocol="HTTP/1.1" redirectPort="8443"/>
 8888로 fix

2. webapp >> WEB-INF folder > web.xml

text this

<?xml version="1.0" encoding="UTF-8"?>
<web-app xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://xmlns.jcp.org/xml/ns/javaee" xsi:schemaLocation="http://xmlns.jcp.org/xml/ns/javaee http://xmlns.jcp.org/xml/ns/javaee/web-app_3_1.xsd" id="WebApp_ID" version="3.1">
	<display-name>Step04_Final</display-name>
  
	<!-- context path 까지만 요청했을때 응답되는 페이지 설정 -->
	<welcome-file-list>
		<welcome-file>index.jsp</welcome-file>
	</welcome-file-list>
  
  	<!-- DB 연동하기 위한 설정 -->
	<resource-ref>
		<description>Oracle Datasource example</description>
		<res-ref-name>jdbc/myoracle</res-ref-name>
		<res-type>javax.sql.DataSource</res-type>
		<res-auth>Container</res-auth>
	</resource-ref>
</web-app>
