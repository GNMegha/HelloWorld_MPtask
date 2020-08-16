# HelloWorld_MPtask

added nodejs app 


1. create the directory named nodejs
2. install npm (if machine is centos do:-)
   2.1)curl -sL https://rpm.nodesource.com/setup_10.x | sudo bash -
   2.2)sudo yum install nodejs
   2.3)node --version
3.create file named package.json in /nodejs directory and paste below file


{
  "name": "docker_web_app",
  "version": "1.0.0",
  "description": "Node.js APP",
  "author": "First Last <meghagn@example.com>",
  "main": "server.js",
  "scripts": {
    "start": "node server.js"
  },
  "dependencies": {
    "express": "^4.16.1"
  }
}


4.create file name itas server.js and paste the code.

5.create file named Dockerfile (placed in the repo)

6. create file named .dockerignore and paste 
node_modules
npm-debug.log

7. then do docker build and build image 

build command:-
docker build -t nodetest/node-web-app .

7. run the build image as container
docker run -p 80:8080 -d nodetest/node-web-app
