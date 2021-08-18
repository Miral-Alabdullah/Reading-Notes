# Using WebSocket to build an interactive web application : 

Manual Initialization (optional)

If you want to initialize the project manually rather than use the links shown earlier, follow the steps given below:

    - Navigate to https://start.spring.io. This service pulls in all the dependencies you need for an application and does most of the setup for you.

    - Choose either Gradle and the language you want to use. This guide assumes that you chose Java.

    - Click Dependencies and select Websocket.

    - Click Generate.

    - Download the resulting ZIP file, which is an archive of a web application that is configured with your choices.

# Adding Dependencies 

```

dependencies {
	implementation 'org.springframework.boot:spring-boot-starter-websocket'
	implementation 'org.webjars:webjars-locator-core'
	implementation 'org.webjars:sockjs-client:1.0.2'
	implementation 'org.webjars:stomp-websocket:2.3.3'
	implementation 'org.webjars:bootstrap:3.3.7'
	implementation 'org.webjars:jquery:3.1.1-1'
	testImplementation 'org.springframework.boot:spring-boot-starter-test'
}

```