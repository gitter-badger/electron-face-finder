## Currently this is only tested on Mac platform. This experimental project is based on the following projects. 
1. [https://github.com/cmusatyalab/openface](https://github.com/cmusatyalab/openface),Apache 2.0 License. Modify its Dockerfile.
2. [https://github.com/yyosifov/image-viewer](https://github.com/yyosifov/image-viewer),  ISC License. Most of UI are from it.

### Known Issues:
1. It seems that sometimes electron side will send partial data to the python sever running in the previous docker container. It may happen when you close the app and immediately restart it and operate it very soon. 

### Todo list
1. add source/targetImage info in the ack packet from server. It is to handle interrupt case. E.g. Change target/source when the process is not finished. 
2. stop button. 

### Install dependencies before running locally
1. Install Docker of Mac if you do not have. Type `sh checkinstallDocker.sh` to install it. Or you can download it from [https://www.docker.com](https://www.docker.com) and then install it.
2. After installing it, type `docker pull grimmer0125/openface-nostartdemo` to install the needed Docker image. Or you can use Docker-UI-tool [kinematic](https://kitematic.com/) to search the docker image and install. 

## How to Run locally

### method 1
1. type `npm start` in terminal. But this way does not have any terminal logs of server side, you need to use [kinematic](https://kitematic.com/) to monitor the server logs from Docker. Or use shell script to attach/exec into the Docker.  

### method 2- Run with monitor server logs directly
1. type `make run` in terminal. In this way, you can see server logs. But you can not use ctrl+c to close Electron-UI app. You need to close it inside Electron app. 

## You can download the packaged binary from here:

# Face Finder/Matcher

A cross-platform Face Matcher based on Electron. It runs on OS X, Windows and Linux. It provides an easy interface to browse a directory of images using the left and right keyboard buttons.

### Caution 
1. It will search all the sub-folders and consume a lot time (1 file-1MB consumes 5s).

# Preview

- OS X:

![alt tag](https://grimmer.io/images/electron-dog.png)

<!--- Windows:-->

<!--![alt tag](http://i.imgur.com/uYsD4yy.png)-->

<!--- Linux:-->

<!--![alt tag](http://i.imgur.com/KXlmv3o.png)-->

# Features

- Find the matched face images. From the menu, `file->open a source file`, select a source image including 1 face. Then click 'open' of menu or click open button , to select folder/any other file. Later it will show matched images.     
- ~~Open a Directory and browse it's images~~
- ~~Open an Image File and browse the images inside the same directory~~
- ~~Fast navigation through the images via Left/Right keyboard buttons~~
- ~~Rotate an image clockwise/anti-clockwise~~
- Save/Move the image to a new location

