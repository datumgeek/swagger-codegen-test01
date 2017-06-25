# swagger-codegen-test01

Generating REST web api service from api.yaml using maven plugin

### create the swagger specs

#### download swagger plugin for IntelliJ

https://plugins.jetbrains.com/plugin/8347-swagger-plugin

![image](https://user-images.githubusercontent.com/22680176/27518753-33460f90-59a4-11e7-8bf0-8aa0b8bbe8a5.png)

#### install swagger spec editor plugin

> * File - Settings: Plugins, Add from disk

![image](https://user-images.githubusercontent.com/22680176/27518778-e7eddb4e-59a4-11e7-8711-d5e3882980e3.png)

#### rough in swagger.yaml

> * Create api.yaml in the "Resources" folder

![image](https://user-images.githubusercontent.com/22680176/27518797-4cfc3788-59a5-11e7-8444-fde9d45424de.png)

#### api.yaml service

![image](https://user-images.githubusercontent.com/22680176/27518823-a56f4fe0-59a5-11e7-8573-54a8f8dd1a4b.png)

#### api.yaml paths

![image](https://user-images.githubusercontent.com/22680176/27518851-172b73ca-59a6-11e7-8e7c-6f3a83260a76.png)

#### api.yaml definitions

![image](https://user-images.githubusercontent.com/22680176/27518867-6c0cb9b2-59a6-11e7-9f27-2607141f0cbe.png)

#### add [swagger-codegen-maven-plugin](https://github.com/swagger-api/swagger-codegen/blob/master/modules/swagger-codegen-maven-plugin/README.md#swagger-codegen-maven-plugin) to pom.xml

![image](https://user-images.githubusercontent.com/22680176/27518890-f93bdca0-59a6-11e7-992b-9c94b5c87c00.png)

#### modify web.xml and add associated classes

![image](https://user-images.githubusercontent.com/22680176/27518914-69d2d78e-59a7-11e7-863c-a97a61edb3bd.png)

![image](https://user-images.githubusercontent.com/22680176/27518929-c63cd27c-59a7-11e7-8318-bcc1d2930298.png)

![image](https://user-images.githubusercontent.com/22680176/27518958-3fbc68b0-59a8-11e7-986b-6880e6985e25.png)

![image](https://user-images.githubusercontent.com/22680176/27518976-a85fbeda-59a8-11e7-9c71-6d349af28259.png)
