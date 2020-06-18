---
layout: post
title: "Spring Boot 소개"
categories: java
---

## What is Spring Boot?

> Spring Boot makes it easy to create stand-alone, production-grade Spring based Applications that you can "just run".   

`Spring Boot`를 사용하면 "단순히 실행"할 수 있는 독립 실행형 Spring 기반 애플리케이션을 쉽게 만들 수 있다. 

> We take an opinionated view of the Spring platform and third-party libraries so you can get started with minimum fuss. Most Spring Boot applications need minimal Spring configuration.

Spring 플랫폼과 third-party 라이브러리를 수용하여, 소란을 최소화 한다.  
대부분 Spring Boot 애플리케이션은 최소한의 스프링 설정이 필요하다.  

## Features 

> Create stand-alone Spring applications

독립 실행형 Spring 애플리케이션을 생성한다. 

> Embed Tomcat, Jetty or Undertow directly (no need to deploy WAR files)

내장형 Tomcat, Jetty, Undertow 포함한다. 

> Provide opinionated 'starter' dependencies to simplify your build configuration

'starter' 컴포넌트 제공, 빌드 설정을 쉽게 할 수 있도록 제공한다. 

> Automatically configure Spring and 3rd party libraries whenever possible

자동으로 Spring, third-party 라이브러리를 설정한다. 

> Provide production-ready features such as metrics, health checks, and externalized configuration

메트릭, 헬스체크, 외부 구성 같은 기능 제공한다. 

> Absolutely no code generation and no requirement for XML configuration

XML 설정을 위해 코드 작성과 요구사항이 필요없다.


## Getting Started 

##### build.gradle
###### starter 컴포넌트 추가

```
dependencies {
    compile("org.springframework.boot:spring-boot-starter-web")    
}
```

##### {PROJECT_NAME}Application.java
###### `@SpringBootApplication`은 `@EnableAutoConfiguration`, `@ComponentScan` 포함  

```java
package com.example.myapplication;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class Application {
    public static void main(String[] args) {
        SpringApplication.run(Application.class, args);
    }

}
```
