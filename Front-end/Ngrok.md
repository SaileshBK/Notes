**Tags**: #ngrok #proxing #front-end #testing

![ng_5-1536x865](https://github.com/SaileshBK/Notes/assets/101400043/ffa19f5d-281f-4e91-93c4-c4afa4a7c9f6)

Link:  [[https://ngrok.com/docs/getting-started/]]

Ngrok is a globally distributed reverse proxy that acts as the front door to your applications, providing a unified ingress platform for delivering traffic from your services to the internet. Ngrok is environment-independent, meaning it can deliver traffic to services running anywhere without requiring changes to your environment's networking setup. 

## Installation

To install Ngrok, follow these steps:

 1) In terminal,
```
	choco install ngrok
```
2) Connect account,
```
	ngrok config add-authtoken <TOKEN>
```
3) Start using the Forwarding tunnel,
```
	ngrok http 4200 --host-header="localhost:4200"
```