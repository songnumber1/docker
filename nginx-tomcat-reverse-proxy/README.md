## docker compose로 nginx tomcat reverse proxy 설정

1. docker-compose.yml 경로 이동
2. docker-compose up -d
3. docker ps 입력하면 nginx-tomcat-reverse-proxy-nginx-1, nginx-tomcat-reverse-proxy-tomcat-1 컨테이너가 실행 상태로 출력
4. cd usr/share/apache-tomcat-8.5.50/webapps/ 입력하여 경로 변경
5. docker cp ROOT.war nginx-tomcat-reverse-proxy-tomcat-1:/usr/local/tomcat/webapps/ 입력하여 리눅스 서버에 ROOT.war 파일을 tomcat 컨테이너 webapps 경로에 ROOT.war 복사
6. localhost 접속 시 Welcome to nginx! 화면 출력
7. localhost/tomcat 접속 시 Apache Tomcat/8.5.98 화면 출력
