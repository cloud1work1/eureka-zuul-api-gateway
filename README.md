# eureka-zuul-api-gateway

## pom.xml spring-boot-starter-netflix-zuul

## Application.java
  `
   @SpringBootApplication
   
   @EnableEurekaClient
   
   @EnableZuulProxy
  `
## application.properties
  `server.port=9000
  
   spring.application.name=ZUUL-API-GATEWAY
   
   eureka.client.serviceUrl.defaultZone=http://localhost:8761/eureka
   
   zuul.prefix=/api
   
   zuul.routes.PRODUCT-SERVICE.path=/product/**
   
   zuul.routes.PRODUCT-SERVICE.service-id=PRODUCT-SERVICE
   
   zuul.routes.CART-SERVICE.path=/cart/**
   
   zuul.routes.CART-SERVICE.service-id=CART-SERVICE
   
   zuul.routes.ORDER-SERVICE.path=/order/**
   
   zuul.routes.ORDER-SERVICE.service-id=ORDER-SERVICE
      
  `
## URL to be followed now will be like http://localhost:9000/api/product/products
