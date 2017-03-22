# springboot


<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
	<modelVersion>4.0.0</modelVersion>
	<groupId>org.sprboot</groupId>
	<artifactId>sprboot</artifactId>
	<version>0.0.1-SNAPSHOT</version>
	<name>sprboot</name>
	<description>sprboot</description>

	<parent>
		<groupId>org.springframework.boot</groupId>
		<artifactId>spring-boot-starter-parent</artifactId>
		<version>1.5.2.RELEASE</version>
	</parent>

	<dependencies>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-web</artifactId>
		</dependency>
	</dependencies>

</project>


--------------------------------------

application.properties

server.port = 8090


--------------------------------------

package org.sprboot.core;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class SprBootInitializer {

	public static void main(String[] args) {
		
		SpringApplication.run(SprBootInitializer.class, args);

	}

}

-----------------------------

package org.sprboot.core.controller;

import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RestController;

@RestController
public class HelloController {

	@RequestMapping("/hello")
	public String getHello() {
		return "Hello";
	}
}
