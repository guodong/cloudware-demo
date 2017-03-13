# cloudware-demo
This document give you a demonstration of cloudware, you can follow the steps bellow to set up an minimal cloudware environment.

## Prerequirement
This demo is build on top of docker environment, you should get the latest docker installed, just follow the instructors of [docker docs](https://docs.docker.com). Host os is not critical, ubuntu server 14.04 is just fine.

Nodejs environment is also needed, follow [Nodejs](https://nodejs.org) to prepare it.

## Setup steps
### Pull the docker image of demonstration

`$ sudo docker pull cloudwarehouse/demo:latest`

### Deploy the cloudware manager server

`$ git clone https://github.com/guodong/cloudware-manager.git`

`$ cd cloudware-manager`

`$ npm install`

`$ sudo nodejs index.js`

NOTE: Command above must be ran as **root**, in order to get access to your docker daemon.

### Deploy the front end desktop environment

`$ cd ../`

`$ git clone https://github.com/guodong/mensa-ng2.git`

`$ cd mensa-ng2`

`$ git checkout demo`

`$ npm install`

`$ npm start`

Then open your browser and visit http://[[your server ip]]:8080, you can see the familar desktop.

The setup script will be published in days as well~

## Tips

* Once you close your browser or just close the page, everything related to your session will be destroyed automaticlly
* Every cloudware will open a random port of your server, you can refresh your page in case of port collision.
