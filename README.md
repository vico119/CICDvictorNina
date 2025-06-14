# Configuracion de Tomcat

1. Cambiar el puerto por defecto para evitar un conflicto de puertos con Jenkins

   <Connector port="9191" protocol="HTTP/1.1"
               connectionTimeout="20000"
               redirectPort="8443" />

3. Configurar los usuarios y roles de Tomcat

 <role rolename="tomcat"/>
  <role rolename="manager-gui"/>
  <user username="admin" password="admin" roles="manager-gui"/>
  <user username="deployer" password="jenkins" roles="manager-script"/>
