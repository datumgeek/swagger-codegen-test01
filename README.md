# swagger-codegen-test01

Generating REST web api service from api.yaml using maven plugin

### See Also: [Java Jersey REST Swagger Angular4+ Recipe](https://github.com/datumgeek/jersey-rest-test03/blob/master/README.md#java-jersey-rest-swagger-angular4-recipe)

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

![image](https://user-images.githubusercontent.com/22680176/27519254-dd26f238-59ac-11e7-9b0b-0faa605a21cd.png)

![image](https://user-images.githubusercontent.com/22680176/27518914-69d2d78e-59a7-11e7-863c-a97a61edb3bd.png)

![image](https://user-images.githubusercontent.com/22680176/27518929-c63cd27c-59a7-11e7-8318-bcc1d2930298.png)

![image](https://user-images.githubusercontent.com/22680176/27518958-3fbc68b0-59a8-11e7-986b-6880e6985e25.png)

![image](https://user-images.githubusercontent.com/22680176/27518976-a85fbeda-59a8-11e7-9c71-6d349af28259.png)

### View generated web api classes

> * remember, these were generated by the swagger codegen maven plugin

![image](https://user-images.githubusercontent.com/22680176/27519032-630eb40c-59a9-11e7-8cd1-869e1dde350e.png)

![image](https://user-images.githubusercontent.com/22680176/27519075-d7a96f6e-59a9-11e7-9b7b-a29277edbccc.png)

![image](https://user-images.githubusercontent.com/22680176/27519109-611f9494-59aa-11e7-894b-bf10d45d70bc.png)

![image](https://user-images.githubusercontent.com/22680176/27519134-d27a9ec2-59aa-11e7-9bd6-d27bff4aceb6.png)

![image](https://user-images.githubusercontent.com/22680176/27519153-2a9909fe-59ab-11e7-8310-c6a3f190a175.png)

![image](https://user-images.githubusercontent.com/22680176/27519208-10fa8daa-59ac-11e7-8428-c9ce030a2770.png)

### Fantastic progress !!  Now let's turn our attention to the Swagger UI

Swagger UI is a web app that works from a swagger.json file (this file is already being generated by our web app at http://localhost:8080/rest/swagger.json)

#### The Swagger UI will look like this (when we've complete the steps below)

![image](https://user-images.githubusercontent.com/22680176/27526138-11e9a1f6-5a01-11e7-8d9e-c127749ab18e.png)

![image](https://user-images.githubusercontent.com/22680176/27526303-0a29e628-5a02-11e7-8e26-ca3488baa5d9.png)

Let's get our Swagger UI implemented:

#### First, Obtain the Swagger UI (static) web files 

Obtain the files from this URL: https://github.com/swagger-api/swagger-ui/tree/master/dist

Copy them to the `src/main/swagger` folder.

![image](https://user-images.githubusercontent.com/22680176/27507653-aa7c4c9c-5890-11e7-9c71-d7a068e0dc1b.png)

#### Edit the Swagger UI "index.html" page to point at our "swagger.json" file

![image](https://user-images.githubusercontent.com/22680176/27507671-0675198e-5891-11e7-935f-68244916fc51.png)

#### Add the swagger UI web files in our project artifacts (File - Project Structure)

![image](https://user-images.githubusercontent.com/22680176/27507685-5eed70a2-5891-11e7-9dbd-1ccdfe09d694.png)

#### Once we have swagger running, we can copy the curl command and run it in the bash shell

![image](https://user-images.githubusercontent.com/22680176/27526175-5768eff2-5a01-11e7-9b3f-5c1f31847895.png)

### Next Steps:

Note: the next logical step is to add the real implementation to the (generated) PlanetsApiServiceImpl.java class, returning a list of planet objects, but I haven't figured out how to do that and still support regenerating the web api from the .yaml to reflect ongoing changes to the web api.

It is possible to do manually, but there must be a better way.  Please stay tuned... :smile:

### Parent / Child --->  Planet / Moons

Now we add a list of moons to the planet object.

#### Here's the ***.yaml***

![image](https://user-images.githubusercontent.com/22680176/27635350-d9185678-5bc3-11e7-9bd0-6b4e7ef2d29a.png)

#### And the resulting Swagger API

![image](https://user-images.githubusercontent.com/22680176/27635474-6311b266-5bc4-11e7-9148-a1012412e0f6.png)

#### At this point, the plan is to take the generated Swagger API Java classes and start a new project [swagger-mongo-test01](https://github.com/datumgeek/swagger-mongo-test01)

> this project will provide an Angular4+ client and MongoDB backend for persistence.

![image](https://user-images.githubusercontent.com/22680176/27635675-3904e69a-5bc5-11e7-9e27-4217cd0bd039.png)
