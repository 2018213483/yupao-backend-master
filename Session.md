# Session共享实现
## 1、安装redis
## 2、引入redis，能够操作redis
```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-data-redis</artifactId>
    <version>2.6.4</version>
</dependency>
```
## 3、引入spring-session和redis的整合，能够将session自动处存储到redis中
```xml
<dependency>
    <groupId>org.springframework.session</groupId>
    <artifactId>spring-session-data-redis</artifactId>
    <version>2.6.3</version>
</dependency>
```
## 4、修改spring-session存储配置 application.yml
```yaml
spring:
    session:
        timeout: 86400
        store-type: redis
```