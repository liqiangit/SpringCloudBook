1修改hosts添加
127.0.0.1 peer1
127.0.0.1 peer2
2 打包
3 执行
java -jar eureka-server-ha-1.0.0.jar --spring.profiles.active=peerl
java -jar eureka-server-ha-1.0.0.jar --spring.profiles.active=peer2
4 访问浏览器
http://localhost:1111/
http://localhost:1112/