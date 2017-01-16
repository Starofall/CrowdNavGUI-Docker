# CrowdNavGUI for Docker

![Banner](https://raw.githubusercontent.com/Starofall/CrowdNavGUI-Docker/master/banner.PNG)


### Description
To see the graphical user interaface of sumo used in [CrowdNav](https://github.com/Starofall/CrowdNav) even with docker,
this special docker container bundles a VNC server and a graphical interface.

### Docker Setup
1) First start kafka

`docker run --name kafka --hostname kafka -p 2181:2181 -p 9092:9092 --env ADVERTISED_HOST=kafka --env ADVERTISED_PORT=9092 spotify/Kafka`

2) Start CrowdNavGUI for Docker

`docker run -i -t --link kafka:kafka -p 6080:6080 starofall/crowdnavgui-docker`

3) Open your browser and goto either
 
`localhost:6080` or `(IP of your Boot2Docker):6080` 
 
4) A VLC session opens. Here click on `startGUI.sh` and then `Execute in Terminal`

5) Now SUMO and CrowdNav is loaded and can be started with the play button