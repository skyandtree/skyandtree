mkdir kikoeru
cd kikoeru
docker run -d --name kikoeru -p 2333:2333 -v $PWD/data:/opt/kikoeru/data -e TZ=Asia/Shanghai -e PUID=$(id -u) -e PGID=$(id -g) -e UMASK=022 --restart unless-stopped vscodev/kikoeru:latest
