1 启动 eureka-server
2 启动 hello-service
3 启动 feign-consumer
4 启动 api-gateway
5 访问浏览器
http://localhost:8083/hello
http://localhost:9001/feign-consumer
http://localhost:5555/api/a/hello
http://localhost:5555/hello-service/hello
http://localhost:5555/feign-consumer/feign-consumer

开启网关
注释掉
zuul.AccessFilter.pre.disable=true
访问浏览器，密切注意，第一个参数要带？而不是&否则request.getParameter("accessToken")==null

http://localhost:5555/api/a/hello
http://localhost:5555/api/a/hello&accessToken=token
http://localhost:5555/api/a/hello?accessToken=token

总结：
在网关里面配置了转发规则
通过
http://localhost:5555/api/a/hello
http://localhost:5555/hello-service/hello
都能访问
# routes to serviceId
zuul.routes.api-a.path=/api/a/**
zuul.routes.api-a.serviceId=hello-service

如果没有配置转发规则
spring.application.name=hello-service
spring.application.name=feign-consumer
通过
http://localhost:5555/hello-service/hello
http://localhost:5555/feign-consumer/feign-consumer
都能访问