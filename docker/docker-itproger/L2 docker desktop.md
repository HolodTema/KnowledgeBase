Способы работать с docker:
-docker desktop - UI desktop app
-docker CLI
-create Dockerfile and Docker compose files to run cmds

## Сейчас работаем с Docker Desktop

```
docker run -d -p 80:80 docker/getting-started
```

**docker run**- запускает контейнер. Если контейнера нет, закачивает его.
(docker run --help в помощь)
- Ключ -d - detach запустить контейнер в фоне и отобразить его id
- Ключ -p - соединяет порты - контейнер будет работать на порту 80 и внутри этого контейнера соединение с нашим ПК будет тоже по порту 80
- Ключ -m - устанавливает лимит памяти для контейнера

**docker pull** - скачивает контейнер

Эта команда запускает контейнер 

Образ (image) - шаблон для запуска контейнеров. Если образ = класс, то контейнер = объект. 

**docker info** - список контейнеров, образов и тд

**docker images** - информация об образах

**docker ps** - информация о контейнерах

Ранее мы запустили getting-started контейнер на 80 порту нашего ПК. Наберем в браузере 0.0.0.0:80 (или localhost:80) - и увидим, что контейнер автоматом задеплоили на определенный порт.

**docker stop %container_id%** (container_id можно найти в docker ps)

**docker start** %container_id% 

**docker pause** %container_id% -контейнер временно не работает

**docker unpause** %container_id%

**docker restart** %container_id%

**docker login** авторизоваться в аккаунте docker

**docker logout** выход из аккаунта




