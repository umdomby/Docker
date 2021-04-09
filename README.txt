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

----------------------------------
docker pull ubuntu
----------------------------------
docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
ubuntu              latest              26b77e58432b        6 days ago          72.9MB
hello-world         latest              d1165f221234        4 weeks ago         13.3kB
----------------------------------
