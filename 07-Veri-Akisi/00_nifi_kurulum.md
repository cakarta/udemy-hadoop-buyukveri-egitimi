# Nifi Kurulum
## 1. Donwload Nifi

```
[root@sandbox-hdp ~]# cd /opt/
[root@sandbox-hdp opt]# wget https://archive.apache.org/dist/nifi/1.9.2/nifi-1.9.2-bin.tar.gz
```

## 2. tar Nifi
` [root@sandbox-hdp opt]# tar xzf nifi-1.9.2-bin.tar.gz `

## 3. Port değiştirme 
` [root@sandbox-hdp opt]# sed -i 's+nifi.web.http.port=8080+nifi.web.http.port=8090+g' nifi-1.9.2/conf/nifi.properties  `

## 4. Port değişikliği kontrol
```
[root@sandbox-hdp opt]# grep 'nifi.web.http.port' nifi-1.9.2/conf/nifi.properties
nifi.web.http.port=8090
```

## 5. JAVA_HOME set
`[root@sandbox-hdp opt]# export JAVA_HOME=/usr/java/default/jre/ `


## 6. Nifi çalıştırma
` [root@sandbox-hdp opt]# nifi-1.9.2/bin/nifi.sh start ` 

## 7. Nifi Web UI
En az 1 dk. bekleyin

Tarayıcıdan
http://sandbox-hdp.hortonworks.com:8090/nifi/
nifi arayüze ulaşınız.



