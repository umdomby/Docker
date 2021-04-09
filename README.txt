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

==================================
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
==================================
docker images
-------------
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
ubuntu              latest              26b77e58432b        6 days ago          72.9MB
hello-world         latest              d1165f221234        4 weeks ago         13.3kB
==================================
