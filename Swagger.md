# swagger配置步骤

## 1、添加swagger的依赖-
```xml
<dependency>
    <groupId>com.github.xiaoymin</groupId>
    <artifactId>knife4j-spring-boot-starter</artifactId>
    <version>2.0.7</version>
</dependency>
```
# 2. 编写配置文件
在配置文件 config 目录下，添加 swagger 的配置文件 SwaggerConfig.java
```java
/**
 * 自定义 Swagger 接口文档的配置
 */
@Configuration// 配置类
@EnableSwagger2WebMvc//自动配置 Swagger 相关的 Bean
//通过在启动应用程序时设置 spring.profiles.active 属性来指定活动配置环境。例如，在 application.properties 文件中设置
// spring.profiles.active=dev
@Profile({"dev", "test"})//基于不同的配置环境为组件或配置类指定特定的配置。
public class SwaggerConfig {
}
```
## 3、application.properties设置
```properties
spring.mvc.path.match.matching-strategy=ant_path_matcher
```