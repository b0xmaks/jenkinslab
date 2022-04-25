FROM tomcat:9.0.20-jre8-alpine
ADD /var/lib/jenkins/workspace/job/target/*.war /usr/local/tomcat/webapps/
CMD ["catalina.sh", "run"]