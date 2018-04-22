1 启动 eureka-server
2 启动 hello-service
3 启动 ribbon-consumer
4 访问浏览器
http://localhost:9000/ribbon-consumer

熔断测试（疑问，hello-service执行完了，熔断有什么用？）

ribbon-consumer
2018-04-22 10:55:36.653  INFO 22044 --- [-HelloService-9] com.didispace.web.HelloService           : Spend time : 2890



hello-service
2018-04-22 10:55:15.976  INFO 6180 --- [nio-8083-exec-1] com.didispace.web.HelloController        : sleepTime:613
2018-04-22 10:55:16.053  INFO 6180 --- [nio-8083-exec-8] com.didispace.web.HelloController        : /hello, host:192.168.125.117, service_id:hello-service
2018-04-22 10:55:16.058  INFO 6180 --- [nio-8083-exec-9] com.didispace.web.HelloController        : /hello1, host:192.168.125.117, service_id:hello-service
2018-04-22 10:55:16.062  INFO 6180 --- [nio-8083-exec-7] com.didispace.web.HelloController        : /hello1, host:192.168.125.117, service_id:hello-service
2018-04-22 10:55:16.067  INFO 6180 --- [nio-8083-exec-4] com.didispace.web.HelloController        : /hello1, host:192.168.125.117, service_id:hello-service
2018-04-22 10:55:16.075  INFO 6180 --- [nio-8083-exec-6] com.didispace.web.HelloController        : /hello3, host:192.168.125.117, service_id:hello-service
2018-04-22 10:55:16.082  INFO 6180 --- [nio-8083-exec-2] com.didispace.web.HelloController        : /hello3, host:192.168.125.117, service_id:hello-service
2018-04-22 10:55:16.591  INFO 6180 --- [nio-8083-exec-1] com.didispace.web.HelloController        : /hello, host:192.168.125.117, service_id:hello-service
2018-04-22 10:55:16.595  INFO 6180 --- [nio-8083-exec-7] com.didispace.web.HelloController        : /hello1, host:192.168.125.117, service_id:hello-service
2018-04-22 10:55:16.600  INFO 6180 --- [nio-8083-exec-4] com.didispace.web.HelloController        : /hello1, host:192.168.125.117, service_id:hello-service
2018-04-22 10:55:16.604  INFO 6180 --- [nio-8083-exec-6] com.didispace.web.HelloController        : /hello1, host:192.168.125.117, service_id:hello-service
2018-04-22 10:55:16.610  INFO 6180 --- [nio-8083-exec-2] com.didispace.web.HelloController        : /hello3, host:192.168.125.117, service_id:hello-service
2018-04-22 10:55:16.623  INFO 6180 --- [nio-8083-exec-1] com.didispace.web.HelloController        : /hello3, host:192.168.125.117, service_id:hello-service
2018-04-22 10:55:17.905  INFO 6180 --- [nio-8083-exec-7] com.didispace.web.HelloController        : sleepTime:1361
2018-04-22 10:55:19.267  INFO 6180 --- [nio-8083-exec-7] com.didispace.web.HelloController        : /hello, host:192.168.125.117, service_id:hello-service
2018-04-22 10:55:19.270  INFO 6180 --- [nio-8083-exec-4] com.didispace.web.HelloController        : /hello1, host:192.168.125.117, service_id:hello-service
2018-04-22 10:55:19.275  INFO 6180 --- [nio-8083-exec-6] com.didispace.web.HelloController        : /hello1, host:192.168.125.117, service_id:hello-service
2018-04-22 10:55:19.277  INFO 6180 --- [nio-8083-exec-2] com.didispace.web.HelloController        : /hello1, host:192.168.125.117, service_id:hello-service
2018-04-22 10:55:19.282  INFO 6180 --- [nio-8083-exec-1] com.didispace.web.HelloController        : /hello3, host:192.168.125.117, service_id:hello-service
2018-04-22 10:55:19.287  INFO 6180 --- [nio-8083-exec-7] com.didispace.web.HelloController        : /hello3, host:192.168.125.117, service_id:hello-service
2018-04-22 10:55:33.765  INFO 6180 --- [nio-8083-exec-4] com.didispace.web.HelloController        : sleepTime:2867
2018-04-22 10:55:36.632  INFO 6180 --- [nio-8083-exec-4] com.didispace.web.HelloController        : /hello, host:192.168.125.117, service_id:hello-service
2018-04-22 10:55:36.636  INFO 6180 --- [nio-8083-exec-6] com.didispace.web.HelloController        : /hello1, host:192.168.125.117, service_id:hello-service
2018-04-22 10:55:36.639  INFO 6180 --- [nio-8083-exec-2] com.didispace.web.HelloController        : /hello1, host:192.168.125.117, service_id:hello-service
2018-04-22 10:55:36.642  INFO 6180 --- [nio-8083-exec-1] com.didispace.web.HelloController        : /hello1, host:192.168.125.117, service_id:hello-service
2018-04-22 10:55:36.648  INFO 6180 --- [nio-8083-exec-7] com.didispace.web.HelloController        : /hello3, host:192.168.125.117, service_id:hello-service
2018-04-22 10:55:36.652  INFO 6180 --- [nio-8083-exec-4] com.didispace.web.HelloController        : /hello3, host:192.168.125.117, service_id:hello-service