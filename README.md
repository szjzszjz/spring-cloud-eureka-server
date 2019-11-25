# spring-cloud-eureka-server
eureka 服务端

### eureka实现高可用  
[eureka高可用操作说明](http://note.youdao.com/noteshare?id=468e8804cb3a5a6235892ad73d394172&sub=7BB28CFB86804FAB974E2974C46B3EC8)  
### 微服务工程启动顺序  
- 1.先启动eureka服务注册中心[spring-cloud-eureka-server](https://github.com/szjzszjz/spring-cloud-eureka-server)  
- 2.启动docker容器，并启动docker容器中的RabbitMQ ([docker容器安装](http://note.youdao.com/noteshare?id=c15879acf30c0d66b33a5dfe6535feba&sub=32FFA5D56FF64B6BB7A0AF8141BEAF30), [RabbitMQ在docker容器中的安装](http://note.youdao.com/noteshare?id=c09c2717d436d4de8cd9d886b77d4c01&sub=D8305095144D470D8C0CBE53F1F6ECB8))   
- 3.启动配置中心[spring-cloud-config](https://github.com/szjzszjz/spring-cloud-config)  
- 4.启动其他的微服务，这些微服务作为`注册中心`和`配置中心`的客户(client)端 
