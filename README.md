## Spring Security OAuth

If you're already a student of Learn Spring Security, you can get started diving deeper into OAuth2 with Module 10, and then Modules 12, 13, and the upcoming module 17. </br></br>
If you're not yet a student, you can get access to the course here: http://bit.ly/github-lss
</br></br></br>



## Build the Project
```
mvn clean install
```



## Projects/Modules
This project contains a number of modules, but here are the main ones you should focus on and run: 
- `spring-security-oauth-server` - the Authorization Server (port = 8081)
- `spring-security-oauth-resource` - the Resource Server (port = 8082)

And, depending on what grant type you want to try out, you'll work with one of these UI/Clients:  
- `angularjs/spring-security-oauth-ui-implicit` (port = 8083)
- `angularjs/spring-security-oauth-ui-password` (port = 8084)

Other Modules: 
- `spring-security-5-oauth-resource` - another version of the Resource Server
- `spring-security-oauth-ui-implicit-angular4` - another version of the Implicit Grant UI Module - using Angular 4
- `spring-security-oauth-ui-password-angular4` - another version of the Password Grant UI Module - using Angular 4

Finally, you can ignore all other modules. 



## Run the Modules
You can run any sub-module using command line: 
```
mvn spring-boot:run
```

If you're using Spring STS, you can also import them and run them directly, via the Boot Dashboard 

You can then access the UI application - for example the module using the Password Grant - like this: 
`http://localhost:8084/`



## Run the Angular 4 Modules

- To run any of Angular4 front-end modules (_spring-security-oauth-ui-implicit-angular4_ and _spring-security-oauth-ui-password-angular4_) , we need to build the app first:
```
mvn clean install
```

- Then we need to navigate to our Angular app directory:
```
cd src/main/resources
```

And run the command to download the dependencies:
```
npm install
```

- Finally, we will start our app:
```
npm start
```
- Note: Angular4 modules are commented out because these don't build on Jenkins as they need npm installed, but they build properly locally
- Note for Angular version < 4.3.0: You should comment out the HttpClient and HttpClientModule import in app.module and app.service.ts. These version rely on the HttpModule.





