###spring中关于mybatis的知识点
####1.mybatis使用generator（mysql）报错：

    Description:
    Failed to configure a DataSource: 'url' attribute is not specified and no embedded datasource could be configured.
    Reason: Failed to determine a suitable driver class
    Action:
    Consider the following:
        If you want an embedded database (H2, HSQL or Derby), please put it on the classpath.
        If you have database settings to be loaded from a particular profile you may need to activate it (no profiles are currently active).
    Process finished with exit code 1
+ 问题原因：
原因是Springboot默认会去扫数据库连接的配置，如果没有在application.properties里面配置好mysql的话，会报错
+ 解决方法： 
    + 在application.properties里面加上mysql相关配置
    + 主程序 中 增加@SpringBootApplication(exclud{DataSourceAutoConfiguration.class} )



