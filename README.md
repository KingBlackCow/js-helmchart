# 각종 라이브러리 명령어 생성 모음
## mysql
```
helm -n ${네임스패이스} install mysql oci://registry-1.docker.io/bitnamicharts/mysql --set primary.persistence.enabled=false --set auth.rootPassword=${root 패스워드}
```

## redis
```
helm -n ${네임스패이스} install redis oci://registry-1.docker.io/bitnamicharts/redis --set architecture=standalone --set auth.enabled=false --set master.persistence.enabled=false
```

## kafka
```
helm -n ${네임스패이스} install kafka oci://registry-1.docker.io/bitnamicharts/kafka --set controller.replicaCount=3  --set sasl.client.passwords=${패스워드} --set controller.persistence.enabled=false --set broker.persistence.enabled=false
```

