# spring-boot-jpa-docker
<!-- PROJECT SHIELDS -->

<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/yewin-mm/spring-boot-jpa-docker.svg?style=for-the-badge
[contributors-url]: https://github.com/yewin-mm/spring-boot-jpa-docker/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/yewin-mm/spring-boot-jpa-docker.svg?style=for-the-badge
[forks-url]: https://github.com/yewin-mm/spring-boot-jpa-docker/network/members
[stars-shield]: https://img.shields.io/github/stars/yewin-mm/spring-boot-jpa-docker.svg?style=for-the-badge
[stars-url]: https://github.com/yewin-mm/spring-boot-jpa-docker/stargazers
[issues-shield]: https://img.shields.io/github/issues/yewin-mm/spring-boot-jpa-docker.svg?style=for-the-badge
[issues-url]: https://github.com/yewin-mm/spring-boot-jpa-docker/issues
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/ye-win-1a33a292/

<h1 align="center">
  Overview
  <img src="https://github.com/yewin-mm/spring-boot-jpa-docker/blob/master/github/template/images/overview/spring_boot_jpa_docker.png" /><br/>
</h1>


# spring-boot-jpa-docker
* This is the sample project for spring-boot with jpa for database operation using docker and build dockerized application and connect to MySQL db container.
* So, purpose is to connect containerized MySQL database from containerized java application and do CRUD operations.

<!-- TABLE OF CONTENTS -->
## Table of Contents
- [About The Project](#about-the-project)
    - [Built With](#built-with)
- [Getting Started](#getting-started)
    - [Before you begin](#before-you-begin)
    - [Clone Project](#clone-project)
    - [Prerequisites](#prerequisites)
    - [Instruction](#instruction)
- [Contact Me](#contact)
- [Contributing](#Contributing)


<a name="about-the-project"></a>
## ⚡️About The Project
This is Demo Project for Spring boot with JPA and running with docker and connect MySQL db container. <br>
As of now, running application as container way is the best option to manage application deployment. (you can find more about benefits of using docker in google). <br>
This project used db as MySQL which is containerized. You can see in here, [MySQL Container](https://github.com/yewin-mm/mysql-docker-container). <br>
You should learn basic Docker Application without application first. You can see in here, [Spring Boot Docker Sample](https://github.com/yewin-mm/spring-boot-docker-sample).


<a name="built-with"></a>
### 🪓 Built With
This project is built with
* [Java](https://www.oracle.com/au/java/technologies/javase/javase-jdk8-downloads.html)
* [Maven](https://maven.apache.org/download.cgi)
* [Containerized MySQL Database](https://github.com/yewin-mm/mysql-docker-container)
* [Docker](https://www.docker.com/products/docker-desktop/)


<a name="getting-started"></a>
## 🔥 Getting Started
This project purpose is to run java application with Spring Boot framework and using JPA for database operation and running as `docker container`. <br>
And also this project purpose is to connect MySQL DB Container. 
This project is built with Java, Maven, MySQL and use `Project Lombok` as plugin.
So, please make sure all are installed in your machine.<br>
- After installation was success, please note that docker will open when you turn on your computer as default and it will take space on RAM of your machine. <br> 
So, you need to set the setting that **not to open always** when you turn on your computer (login account) to reduce unnecessary taking space when you are not using related with docker.
- Open `docker desktop` and you can see `docker icon` which are at noti bar. (Window user need to expand arrow which bottom right corner to see docker icon whereas Mac user can see at top noti bar).
- `Right click` on docker icon and click `Dashboard`, after docker desktop was open, click `setting icon` (top right corner) and `uncheck` (untip) mark on `“Start Docker Desktop when you login”` in `General` tab. Click `“Apply & Restart”`.
- With that setting, you can close, open whatever you want and it **will not open always** when you turn on your computer anymore.


<a name="before-you-begin"></a>
### 🔔 Before you begin
If you are new in Git, GitHub and new in Spring Boot configuration structure, <br>
You should see basic detail instructions first in here [Spring Boot Application Instruction](https://github.com/yewin-mm/spring-boot-app-instruction)<br>
If you are not good enough in basic API knowledge with Java Spring Boot, Docker basic and other spring basic knowledge, you should learn below example projects first. <br>
Click below links.
* [Spring Boot Sample CRUD Application](https://github.com/yewin-mm/spring-boot-sample-crud) (for sample CRUD application)
* [Reading Values from Properties files](https://github.com/yewin-mm/reading-properties-file-values) (for reading values from properties files)
* [Spring Boot Docker Sample](https://github.com/yewin-mm/spring-boot-docker-sample)
* [MySQL Container](https://github.com/yewin-mm/mysql-docker-container)


<a name="clone-project"></a>
### 🥡 Clone Project
* Clone the repo
   ```sh
   git clone https://github.com/yewin-mm/spring-boot-jpa-docker.git
   ```
<a name="prerequisites"></a>
### 🔑 Prerequisites
Prerequisites can be found here, [Spring Boot Application Instruction](https://github.com/yewin-mm/spring-boot-app-instruction). <br>
Docker prerequisites can be found here, [Spring Boot Docker Sample](https://github.com/yewin-mm/spring-boot-docker-sample). <br>


<a name="instruction"></a>
### 📝 Instruction
* First of all, create your database by using database GUI tools like DBeaver or Datagrip or Workbench or type in MySQL container console by running `create database {your db name which inside properties file};`.
* Eg. query `create database spring_boot_jpa_docker;`. 
* (Without Using Docker) If you don't want to use docker and just for testing application, 
  * In application properties, Uncomment `localhost` db url line in spring datasource and comment out `yw_mysql` db url line.
  * Your machine need to be installed MySQL db already. 
  * You can install either with normal MySQL db installer or your can run [MySQL db as Container](https://github.com/yewin-mm/mysql-docker-container).
  * After that, you can directly run the project in your IDE. 
  * But this project purpose is to run as containerized application and connect to MySQL db container.
* (With Docker), Open Docker Desktop in your machine. (Start docker).
* First of all, you can check Dockerfile which under project folder.
* You can't run your application as container without that Dockerfile. 
* Go to your application folder with command prompt CMD (for window) or Terminal (for Mac and Linux) or you can also open your IDE Terminal while you opening the project with your IDE. <br>
* Below commands need to type in your `CMD` or `Terminal` where path should be in your application folder.
* Generate jar file
  * Type -> `mvn clean package -DskipTests=true` 
  * Here, if you don't add skipTest, it will get compile time error because your application will try to connect to MySQL container as per application.properties file config db url. 
  * Because if you want to connect to MySQL container, you need to add container name in datasource url of properties file and that url can't be resolved from your local. 
  * You can also type `mvn clean install -DskipTests=true`.
* Check docker version to make sure your installed docker is up or down by typing `docker --version`, 
* If you can't see docker version by above command, you need to open docker (docker desktop) or something wrong with your installation process for docker. Check more about docker installation error in google.
* Check your MySQL container is up or down by typing `docker ps`.
* If you can't see your MySQL container, you need to run MySQL db as container. See in here, [MySQL db Container](https://github.com/yewin-mm/mysql-docker-container).
* Create docker image
  * Before do below build command, 
    * Please make sure Docker Desktop (Docker service) is open in your machine.
    * Please make sure your generated jar file (generate with above `mvn clean package -DskipTests`) is under target folder.
    * Because docker build image will read `Dockerfile` and do process as per `Dockerfile`, So, if your jar file name is not same with `Dockerfile`, you can't create image.
    * Please make sure your jar file name under target folder and jar file name in `COPY` keyword of `Dockerfile` must be same.
    * Please make sure your MySQL db container is up in docker engine. (check with `docker ps`)
    * Please make sure your MySQL db container name and your application properties file db url are same.
  * If all are ok, create your application to docker image by below command.
  * Type
    ```sh
    docker build -t spring-boot-jpa-docker .
    ```
  * In there, you can define your application image name as you want instead of spring-boot-jpa-docker.
  * In there, you need to add dot `(.)` at the end of build command by spacing.
  * In there, you can add tag version after application name like below, if you don't set tag version, the application will go with tag version: latest as default.
  * with tag version -> `docker build -t spring-boot-jpa-docker:1.0 .`

  * You can check your created docker images with below command.
  * ```sh
    docker images
    ```
  * Here, you can see Repository (image name), Tag (version), Image Id, Created date, etc.

* Run docker images as container
  * Docker will run as container by reading image, So, please make sure your image is already created.
  * Please make sure your created database is existed in MySQL database which I mentioned first step.
  * Type
    ```sh
    docker run --net=mysql -d -p 8080:8080 spring-boot-jpa-docker
    ```
  * In there, --net is tell this application to run under mysql network. 
  * If we don't add that network, you can't connect to MySQL database and application can't be started because our MySQL db Container is running under that `mysql` network. [MySQL db Container](https://github.com/yewin-mm/mysql-docker-container).
  * You can also use --network instead of --net in here, those two are same.
  * In there, -d is detached mode and if we put -d in docker, application logs will be hidden and run in background.
  * If your application can't call well, can't start you can remove `-d` option to see the running logs.
  * If your application was running well, you can shut down application by clicking `ctrl+c` and can start the application by adding `-d` option again.
  * You can check your container is running or not by typing `docker ps`.
  * -p is port which we need to add and bind with tcp port.
  * in -p 8080:8080,
    * the last 8080 is the port which run inside docker, and it's need to same with the port which we added in application.properties file.
    * the first 8080 is the port which can call from outside and bind with inside running port 8080.
    * So, you can change the first port it to other ports like -p 9090:8080, and if so, you need to call the api of application by using 9090 port.
    * the last word is your image name and if you set tag version when you create image, <br>
    you need to add that version in run command like `docker run --net=mysql -d -p 8080:8080 spring-boot-jpa-docker:1.0`

* Check container
  * Type (check running containers)
      ```sh
      docker ps
    
  * Here, you can see Container Id, Image name, etc.

* If your application is not running well when application started up, you can check logs by removing `-d` to appear log in CMD or Terminal like below. <br>
 run without detached mode `docker run --net=mysql -p 8080:8080 spring-boot-jpa-docker` <br>
 you can stop (terminate) application by pressing Ctrl+C when you run application without detached mode. <br>
* For more error debugging, logging and other docker commands, you can find in below,
  * [Dockerized Application Sample Commands, error debugging and watch logging](https://github.com/yewin-mm/spring-boot-docker-sample/blob/master/README.md#instruction)


* If you run application with detached mode and if you want to stop application, you can stop container.
* Please note that If you don't stop container, your application will run background the whole time.
  * Type
    ```sh
    docker stop {container_id}
  * here, you can get your application container id by typing `docker ps`. (If your container is already stopped, you cannot see that by `docker ps` and you need to find stopped containers with `docker ps -a`).
  * copy your container id and put it instead {} brackets variable. eg. `docker stop 12077ee7d46f`

* If you want to start the application next time, you can start application easily with below command.
* Please note that, you don't need to create `image` again, and you don't need to run `image` again if you want to re-start application which is stopped.
* That is the one of the good approach using container for running application. All you need is just `start` and `stop` to run, stop your application.
  * Type
    ```sh
    docker start {container_id}
    ```
  * You don't need to type `docker run` again. Just need to type start and id.
  * here, you can get your stopped application container id by typing `docker ps -a`.
  * here, `-a` flag is because if you stopped container, you cannot see that container id by typing `docker ps`. That's why need to put `-a` to get stopped container id.

* Check Docker disk space as some unnecessary images and unused containers may take much space
  * Type 
    ```sh
    docker system df
    ```

* For more commands like, cleaning unused containers, images, get inside container, logging, deleting container, image
  * you can find in here, [Dockerized Application Sample Commands](https://github.com/yewin-mm/spring-boot-docker-sample/blob/master/README.md#instruction)

* Testing
  * Import `spring-boot-jpa-docker.postman_collection.json` file under project directory (see that file in project directory) into your installed Postman application.
    * Click in your Postman (top left corner) import -> file -> upload files -> {choose that json file} and open/import.
    * After that, you can see the folder which you import from file in your Postman.
  * Now, you can 'Test' this project by calling API from Postman.
    * Open your imported folder in postman and inside this folder, you will see total of 3 APIs, you can test that all APIs by clicking `Send` button one by one and see the response.
    * You can also check in your docker container logs for some print out values.
    * You can check data in DB by using Database GUI tools like DBeaver or Datagrip or Workbench or you can select query inside MySQL Container.

* After that you can see the code and check the code and docker file and check containerized MySQL DB which you don't know. You can learn it, and you can apply in your job or study fields.

***Have Fun and Enjoy in Learning Code***


<a name="contact"></a>
## ✉️ Contact
Name - Ye Win <br> LinkedIn profile -  [Ye Win's LinkedIn](https://www.linkedin.com/in/ye-win-1a33a292/)  <br> Email Address - yewin.mmr@gmail.com

Project Link: [Spring Boot JPA Docker](https://github.com/yewin-mm/spring-boot-jpa-docker)


<a name="contributing"></a>
## ⭐ Contributing
Contributions are what make the open source community such an amazing place to be learnt, inspire, and create. Any contributions you make are **greatly appreciated**.
<br>If you want to contribute....
1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/yourname`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeatures'`)
4. Push to the Branch (`git push -u origin feature/yourname`)
5. Open a Pull Request
