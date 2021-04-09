https://docs.docker.com/engine/install/linux-postinstall/
https://hub.docker.com/search/?q&type=image

# Docker
Создайте группу докеров, если она не существует
$ sudo groupadd docker
Добавьте своего пользователя в группу докеров.
$ sudo usermod -aG docker $USER
Выполните следующую команду или выйдите из системы и снова войдите в систему и запустите (это не сработает, вам может потребоваться сначала перезагрузить компьютер)
$ newgrp docker

Проверьте, можно ли запустить докер без рута
$ docker run hello-world
Перезагрузитесь, если ошибка не исчезла.

$ reboot

==============================
docker pull ubuntu
------------------
Using default tag: latest
latest: Pulling from library/ubuntu
a70d879fa598: Pull complete 
c4394a92d1f8: Pull complete 
10e6159c56c0: Pull complete 
Digest: sha256:3c9c713e0979e9bd6061ed52ac1e9e1f246c9495aa063619d9d695fb8039aa1f
Status: Downloaded newer image for ubuntu:latest
docker.io/library/ubuntu:latest
=============================
docker images
-------------
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
ubuntu              latest              26b77e58432b        6 days ago          72.9MB
hello-world         latest              d1165f221234        4 weeks ago         13.3kB
=============================
docker run -it ubuntu        |   go to докер
---------------------
root@23a473346b10:/#
=============================
root@23a473346b10:/# ls
                     --
bin   dev  home  lib32  libx32  mnt  proc  run   srv  tmp  var
boot  etc  lib   lib64  media   opt  root  sbin  sys  usr
=============================
root@23a473346b10:/# exit
=============================
docker ps -a                 |   see worker container
=============================
docker rm dreamy_maxwell     |   удалить контейнер dreamy_maxwell
=============================
docker rm $(docker ps -aq)   |   удалить все контейнеры
=============================
docker images                |   see load container
=============================
docker rmi $(docker images -q) | dell all image
=============================
docker images a              | see images
=============================
docker run -it alpine sh     |  start in console shell
=============================
ls                           | see folder
=============================
apk add bash                 | add package menager
=============================
bash                         | in to bash
----
bash-5.1# 
=============================
exit
====
exit
====
docker ps
========
docker stop container_name | stop container
==========================
docker start container_name | stop container
==========================
docker run -d --name pg postgres | start backgraund postgres name : pg
or
docker run --rm   --name pg-docker -e POSTGRES_PASSWORD=docker -d -p 5432:5432 -v $HOME/docker/volumes/postgres:/var/lib/postgresql/data  postgres
psql -h localhost -U postgres -d postgres
password: docker
==========================
ctop
----
sudo wget https://github.com/bcicen/ctop/releases/download/v0.7.1/ctop-0.7.1-linux-amd64 -O /usr/local/bin/ctop
sudo chmod +x /usr/local/bin/ctop
==========================
docker pull postgres:12
==========================
sudo service postgresql stop
==========================
docker exec -it pg-docker bash  | in settings


