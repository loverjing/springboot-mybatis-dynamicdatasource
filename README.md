# This is springboot-mybatis-dynamicdatasource
- springboot+mybatis+druid+mysql实现的服务启动时加载多数据源、运行时数据源动态切换
- Druid是阿里巴巴开源平台上一个数据库连接池实现，使用Druid可以实现DAO层数据源动态切换
- 数据源加载方式1（dev环境下）：服务启动时通过jdbc读取主数据库中关于数据源的配置来加载数据源，添加/修改/删除数据源时只需在主数据库中配置，然后重启服务，无需代码改动
- 数据源加载方式2（test环境下）：服务启动时通过读取配置文件(config/application-test.properties)中关于数据源的配置来加载数据源，添加/修改/删除数据源时只需在配置文件中配置，然后重启服务，无需代码改动

# test
- 在创建好数据库并初始化数据之后，通过swagger或者直接访问http://localhost:8080/mybatis/getDataBases?dataSource=XXX链接查看数据源动态切换的效果

## Guide
https://github.com/yjclsx/springboot-mybatis-dynamicdatasource.git

## What you'll need
- JDK 1.8+
- Maven 3+

## Stack
- Java
- Spring Boot

## author
- yaojiacheng