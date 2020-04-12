# docker-jenkins-nginx
A Jenkins + Nginx reverse proxy Docker container

# How to run the containers
`$ git clone https://github.com/lainatnavi/docker-jenkins-nginx`
`$ cd docker-jenkins-nginx`
`$ docker-compose up -d`

Nginx binds to port 80<br>
Username: Admin<br>
Password: auto generated<br>
`http://ip-or-dns/`
<br>
Retrieve Jenkins Admin user password:<br>
`docker exec jenkins_master_1 cat /var/jenkins_home/secrets/initialAdminPassword`

<br>Tested with Docker version 18.09.9, build 1752eb3. <br>docker-compose version 1.23.2

