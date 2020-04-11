# docker-jenkins-nginx
A Jenkins + Nginx reverse proxy Docker container

# How to run this container
`git clone https://github.com/lainatnavi/docker-jenkins-nginx`

`cd docker-jenkins-nginx`

`docker-compose up -d`

Nginx binds to port 80
Username: Admin
Password: auto generated
`http://ip-or-dns/`

Retrieve Jenkins Admin user password
`docker exec jenkins_master_1 cat /var/jenkins_home/secrets/initialAdminPassword`


