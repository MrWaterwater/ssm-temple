**该项目作为SSM框架模板**

内有详细注释，自己看

整个项目结构如下

controller为控制包

pojo为实体类包

dao为数据层包，实现接口

service为事务包

![image-20201222220417981](C:\Users\WangShuishui\AppData\Roaming\Typora\typora-user-images\image-20201222220417981.png)

spring-dao.xml用于整合spring和mybatis

spring-mvc用于整合spring和spingMVC

spring-service用于整合spring和事务

applicationContext.xml用于联立配置文件

![image-20201222220605321](C:\Users\WangShuishui\AppData\Roaming\Typora\typora-user-images\image-20201222220605321.png)

在IDEA中，pom.xml文件中的

<build>

</build>

中需要加上这段代码，用于解决资源文件路径问题

``` xml
<resources>
      <resource>
        <directory>src/main/java</directory>
        <includes>
          <include>**/*.properties</include>
          <include>**/*.xml</include>
        </includes>
        <filtering>false</filtering>
      </resource>
      <resource>
        <directory>src/main/resources</directory>
        <includes>
          <include>**/*.properties</include>
          <include>**/*.xml</include>
        </includes>
        <filtering>false</filtering>
      </resource>
    </resources>
```

