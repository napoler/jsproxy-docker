# jsproxy-docker


## 打包

docker build ./ -t js/temp


docker run -d -p 8080:8080 js/temp:latest


docker exec -it 555da7805eb4 sh

交互进入

docker run -p 8082:8080 -it js/temp:latest bash
