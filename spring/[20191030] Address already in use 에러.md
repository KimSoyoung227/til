# 20191030

### BindException : Address already in use
```

  .   ____          _            __ _ _
 /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
 \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
  '  |____| .__|_| |_|_| |_\__, | / / / /
 =========|_|==============|___/=/_/_/_/
 :: Spring Boot ::        (v2.1.4.RELEASE)

2019-10-30 21:13:33.977  INFO 15308 --- [           main] com.gaesenak.web.WebApplication          : Starting WebApplication on LAPTOP-K194IIK4 with PID 15308 (C:\Users\ss\git\web_boot\bin\main started by ss in C:\Users\ss\git\web_boot)
2019-10-30 21:13:34.180  INFO 15308 --- [           main] com.gaesenak.web.WebApplication          : No active profile set, falling back to default profiles: default
2019-10-30 21:13:38.539  WARN 15308 --- [           main] o.m.s.mapper.ClassPathMapperScanner      : No MyBatis mapper was found in '[com.gaesenak.web.mapper.TestUserMapper]' package. Please check your configuration.
2019-10-30 21:13:44.859  INFO 15308 --- [           main] o.s.b.w.embedded.tomcat.TomcatWebServer  : Tomcat initialized with port(s): 8888 (http)
2019-10-30 21:13:45.007  INFO 15308 --- [           main] o.apache.catalina.core.StandardService   : Starting service [Tomcat]
2019-10-30 21:13:45.009  INFO 15308 --- [           main] org.apache.catalina.core.StandardEngine  : Starting Servlet engine: [Apache Tomcat/9.0.17]
2019-10-30 21:13:46.527  INFO 15308 --- [           main] org.apache.jasper.servlet.TldScanner     : At least one JAR was scanned for TLDs yet contained no TLDs. Enable debug logging for this logger for a complete list of JARs that were scanned but no TLDs were found in them. Skipping unneeded JARs during scanning can improve startup time and JSP compilation time.
2019-10-30 21:13:46.554  INFO 15308 --- [           main] o.a.c.c.C.[Tomcat].[localhost].[/]       : Initializing Spring embedded WebApplicationContext
2019-10-30 21:13:46.555  INFO 15308 --- [           main] o.s.web.context.ContextLoader            : Root WebApplicationContext: initialization completed in 11611 ms
2019-10-30 21:13:48.379  INFO 15308 --- [           main] o.s.s.concurrent.ThreadPoolTaskExecutor  : Initializing ExecutorService 'applicationTaskExecutor'
2019-10-30 21:13:48.870  INFO 15308 --- [           main] o.s.b.a.w.s.WelcomePageHandlerMapping    : Adding welcome page template: index
2019-10-30 21:13:49.485 ERROR 15308 --- [           main] org.apache.catalina.util.LifecycleBase   : Failed to start component [Connector[HTTP/1.1-8888]]

org.apache.catalina.LifecycleException: Protocol handler start failed
	at org.apache.catalina.connector.Connector.startInternal(Connector.java:1008) ~[tomcat-embed-core-9.0.17.jar:9.0.17]
	at org.apache.catalina.util.LifecycleBase.start(LifecycleBase.java:183) ~[tomcat-embed-core-9.0.17.jar:9.0.17]
	at org.apache.catalina.core.StandardService.addConnector(StandardService.java:226) [tomcat-embed-core-9.0.17.jar:9.0.17]
	at org.springframework.boot.web.embedded.tomcat.TomcatWebServer.addPreviouslyRemovedConnectors(TomcatWebServer.java:259) [spring-boot-2.1.4.RELEASE.jar:2.1.4.RELEASE]
	at org.springframework.boot.web.embedded.tomcat.TomcatWebServer.start(TomcatWebServer.java:197) [spring-boot-2.1.4.RELEASE.jar:2.1.4.RELEASE]
	at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.startWebServer(ServletWebServerApplicationContext.java:311) [spring-boot-2.1.4.RELEASE.jar:2.1.4.RELEASE]
	at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.finishRefresh(ServletWebServerApplicationContext.java:164) [spring-boot-2.1.4.RELEASE.jar:2.1.4.RELEASE]
	at org.springframework.context.support.AbstractApplicationContext.refresh(AbstractApplicationContext.java:552) [spring-context-5.1.6.RELEASE.jar:5.1.6.RELEASE]
	at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.refresh(ServletWebServerApplicationContext.java:142) [spring-boot-2.1.4.RELEASE.jar:2.1.4.RELEASE]
	at org.springframework.boot.SpringApplication.refresh(SpringApplication.java:775) [spring-boot-2.1.4.RELEASE.jar:2.1.4.RELEASE]
	at org.springframework.boot.SpringApplication.refreshContext(SpringApplication.java:397) [spring-boot-2.1.4.RELEASE.jar:2.1.4.RELEASE]
	at org.springframework.boot.SpringApplication.run(SpringApplication.java:316) [spring-boot-2.1.4.RELEASE.jar:2.1.4.RELEASE]
	at org.springframework.boot.SpringApplication.run(SpringApplication.java:1260) [spring-boot-2.1.4.RELEASE.jar:2.1.4.RELEASE]
	at org.springframework.boot.SpringApplication.run(SpringApplication.java:1248) [spring-boot-2.1.4.RELEASE.jar:2.1.4.RELEASE]
	at com.gaesenak.web.WebApplication.main(WebApplication.java:19) [main/:na]
Caused by: java.net.BindException: Address already in use: bind
	at sun.nio.ch.Net.bind0(Native Method) ~[na:1.8.0_191]
	at sun.nio.ch.Net.bind(Unknown Source) ~[na:1.8.0_191]
	at sun.nio.ch.Net.bind(Unknown Source) ~[na:1.8.0_191]
	at sun.nio.ch.ServerSocketChannelImpl.bind(Unknown Source) ~[na:1.8.0_191]
	at sun.nio.ch.ServerSocketAdaptor.bind(Unknown Source) ~[na:1.8.0_191]
	at org.apache.tomcat.util.net.NioEndpoint.initServerSocket(NioEndpoint.java:236) ~[tomcat-embed-core-9.0.17.jar:9.0.17]
	at org.apache.tomcat.util.net.NioEndpoint.bind(NioEndpoint.java:210) ~[tomcat-embed-core-9.0.17.jar:9.0.17]
	at org.apache.tomcat.util.net.AbstractEndpoint.bindWithCleanup(AbstractEndpoint.java:1103) ~[tomcat-embed-core-9.0.17.jar:9.0.17]
	at org.apache.tomcat.util.net.AbstractEndpoint.start(AbstractEndpoint.java:1189) ~[tomcat-embed-core-9.0.17.jar:9.0.17]
	at org.apache.coyote.AbstractProtocol.start(AbstractProtocol.java:568) ~[tomcat-embed-core-9.0.17.jar:9.0.17]
	at org.apache.catalina.connector.Connector.startInternal(Connector.java:1005) ~[tomcat-embed-core-9.0.17.jar:9.0.17]
	... 14 common frames omitted

2019-10-30 21:13:49.624  INFO 15308 --- [           main] o.apache.catalina.core.StandardService   : Stopping service [Tomcat]
2019-10-30 21:13:49.665  INFO 15308 --- [           main] ConditionEvaluationReportLoggingListener : 

Error starting ApplicationContext. To display the conditions report re-run your application with 'debug' enabled.
2019-10-30 21:13:49.673 ERROR 15308 --- [           main] o.s.b.d.LoggingFailureAnalysisReporter   : 

***************************
APPLICATION FAILED TO START
***************************

Description:

The Tomcat connector configured to listen on port 8888 failed to start. The port may already be in use or the connector may be misconfigured.

Action:

Verify the connector's configuration, identify and stop any process that's listening on port 8888, or configure this application to listen on another port.

2019-10-30 21:13:49.694  INFO 15308 --- [           main] o.s.s.concurrent.ThreadPoolTaskExecutor  : Shutting down ExecutorService 'applicationTaskExecutor'
```


- 메시지 내용 : 포트 이미 사용중이므로 서버를 올릴 수 없음.
- 해결한 방법 : 포트 kill 후, 다시 시작해서 해결

1. netstat -nao | findstr <port>
2. taskkill /f /pid <pid>
