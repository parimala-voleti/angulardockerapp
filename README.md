# angulardockerapp
1. sudo apt-get update
sudo apt-get install build-essential checkinstall libssl-dev
For installing npm lates : hostingadvice.com/how-to/update-node-js-latest-version/
command -v nvm ---> to chk if nvm is intalled --node version manager
nvm install node (ther are diffeenrt wys o snas --can use npm also)

parimalavoletim@parimalavoletim:~$ node -v
v13.13.0
parimalavoletim@parimalavoletim:~$ docker -v
Docker version 18.09.7, build 2d0083d
parimalavoletim@parimalavoletim:~$ npm -v
6.14.4
parimalavoletim@parimalavoletim:~$ npm install -g @angular/cli@7.3.9
sudo chown -R $USER:$(id -gn $USER) /home/parimalavoletim/.config

ng new angulardockerapp
cd angulardockerapp

parimalavoletim@parimalavoletim:~/angulardockerapp$ vim Dockerfile

parimalavoletim@parimalavoletim:~/angulardockerapp$ vim .dockerignore

parimalavoletim@parimalavoletim:~/angulardockerapp$ docker build -t example:dev .

parimalavoletim@parimalavoletim:~/angulardockerapp$ docker run -d -v ${PWD}:/app -v /app/node_modules -p 4201:4200 --rm example:dev 

