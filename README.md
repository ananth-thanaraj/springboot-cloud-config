# springboot-cloud-config

Testing the application

#Test the end-to-end result by starting the Config Service first and then, once loaded, starting the client. 
Visit the client app in the browser, http://localhost:8889/message. 
There, you should see the String Hello world reflected in the response.

#Change the message key in the a-bootiful-client.properties file in the Git repository to something different (Hello Spring!, perhaps?). 
You can confirm that the Config Server sees the change by visiting http://localhost:8888/bootiful-client/default. 
You need to invoke the refresh Spring Boot Actuator endpoint in order to force the client to refresh itself and draw the new value in. 
Spring Boot\u2019s Actuator exposes operational endpoints, like health checks and environment information, about an application. 
In order to use it you must add org.springframework.boot:spring-boot-starter-actuator to the client app\u2019s CLASSPATH. 
You can invoke the refresh Actuator endpoint by sending an empty HTTP POST to the client\u2019s refresh endpoint,
http://localhost:8889/refresh, and then confirm it worked by reviewing the http://localhost:8889/message endpoint.
