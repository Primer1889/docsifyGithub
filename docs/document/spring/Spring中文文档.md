# Springboot 中文文档

## 1、入门

### 1.1 环境

- jdk 要求 java17【OK】

官网下载 jdk 压缩包之后解压，然后进入 cd ~ 目录，配置 .bash_profile 文件，最后使配置生效 source .bash_profile

```shell
JAVA_HOME=/Users/jsonli/Desktop/Primer/env/jdk/jdk-17.0.8.jdk/Contents/Home
PATH=$JAVA_HOME/bin:$PATH
export JAVA_HOME
export PATH
```

- brew install maven

如果出现无法安装错误提示，可执行 brew update 更新后再尝试安装

- servlet 容器

安装 tomcat

- gradle 7.x
`brew install gradle`

如果觉得下载太慢还不如直接去官网下载二进制文件
```shell
export PATH=$PATH:/Users/jsonli/Desktop/Primer/env/gradle/gradle-8.3/bin
export GRADLE=/Users/jsonli/Desktop/Primer/env/gradle/gradle-8.3
export PATH=$PATH:$GRADLE/bin
```

- spring boot CLI

查看是否已存在 spring-io/tap：brew tap

不存在则先执行 brew tap spring-io/tap

然后执行 brew install spring-boot


### 1.2 第一个知识点

@RestController
- 将用于处理客户端请求
- 告诉 spring 将返回的结果直接响应给客户端

@RequestMapping
- 提供路由信息，映射到当前方法，由此方法处理此请求

@SpringBootApplication
-  元注解，写在启动类上
- 启动组件扫描
- 启用自动配置机制

@EnableAutoConfiguration
- 与 starter 配合，比如对于 spring-boot-starter-webspring 将会自动配置 tomcat 和 spring mvc

@Configuration
- spring 自定义配置

@ComponentScan
- 自动扫描加载 spring 组件 

@Autowried
- 告诉 spring 该使用那个构造函数进行依赖注入

