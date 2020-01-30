# docker-http2-benchmark

## 1. 准备工作

### 1.1 签发证书

参考文档[Certificates for localhost](https://letsencrypt.org/docs/certificates-for-localhost/), 为 `localhost`域名签发证书.

执行
``` 
chmod +x create_ssl.sh
./create_ssl.sh
```

将证书 `ssl/localhost.crt` 加入到系统可信证书列表中.

对于 mac 系统, 在Mac上打开“钥匙串访问”，然后转到“系统”中的证书列表，通过点击+号按钮导入证书localhost.crt.

### 1.2 搭建 http2 服务环境

```
cd server
mkdir -p log
docker-compose up -d
```



