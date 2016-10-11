# NotesforDocker

1.删除image 为none的
docker rmi $(docker images | awk '/^<none>/ { print $3 }')
2.docker run -p hostPort:containerPort image
通常情况下 默认是tcp 如需指定
需要
docker run -p 2000：3000/udp ...
如果省略 hostPort  docker会自动配置hostPort
查询hostPort 需要
docker port containerID
