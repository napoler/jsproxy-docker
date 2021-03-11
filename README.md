# jsproxy-docker


## 打包

docker build ./ -t js/temp


docker run -d -p 8080:8080 js/temp:latest


docker exec -it 555da7805eb4 sh

交互进入

#docker run -p 8082:8080 -v /home/terry/dev/proxy/code/jsconf/:/home/jsproxy  -it js/temp:latest bash

docker run -p 8082:8080 -v /home/terry/dev/proxy/code/jsconf/:/home/jsproxy  -it js/temp:latest bash


# 切换到 jsproxy 用户
su - jsproxy

# 重启服务
./run.sh reload

# 关闭服务（参数和 nginx -s 相同）
./run.sh quit

# 启动服务
./run.sh

# 查看代理日志
tail server/nginx/logs/proxy.log
