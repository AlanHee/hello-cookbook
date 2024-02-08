## docker why
- deploy just in minutes inssert serval day before
- effect the enviroment develop due

### helloworld
```
docker run ubuntu:15.10 /bin/echo "Hello world"
```
### check
```
docker ps                   list runing contains
docker logs id              print std out 
docker port                 list port 
docker top id               list process
docker inspect id           info
```
### run
```
#-t:as terminal
#-i:interaction
docker run -i -t ubuntu:15.10 /bin/bash

#-d deamo
docker run -d ubuntu:15.10 /bin/sh -c "while true; do echo hello world; sleep 1; done"

-P:map to localhost
-p:map to localhost as your deine: 
eg: -p 5000:5000
eg: -p 127.0.0.1:5001->5002/tcp   

docker run -d -P --name youj training/webapp python app.py
--name define a contain name repace as id 

```

### stop
```
docker stop id
```

### images
```
#list
docker images

#search
docker search 

#create
#1. just run ... 
#2. docker build with .Dockerfile

docker build -t youj/centos:6.7 .
-t ：target name
. ：Dockerfile path

#update
docker commit -m="has update" -a="youj" e218edb10161 w3cschool/ubuntu:v2
-m:'message'
-a: auhor
e218edb10161：contain id
w3cschool/ubuntu:v2:target org/image:version
```

### tag
```
docker tag 860c279d2fec youj/centos:dev
```

