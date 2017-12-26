# myRemoteBell

## Idea:
Using esp8266 to ring a bell via the Internet
Features:
* Remote bell
* Display caller Info
* Send Response (Decline/Wait/NoAnswer)
* Smart Config
* Pass voice
* Temperature acquire

## To-do:
* [ ] Develop BackEnd
  * [x] Setup public server
  * [x] Setup MQTT broker (authen, tls)
  * [ ] Device Management
* [ ] Develop Device
  * [ ] Prep devices
    * [ ] ESP8266
    * [ ] Power Adaptor
    * [ ] Bell (buzzer)
* [ ] Develop WebApp
  * [ ] Login
  * [ ] Call (ring a bell)
* [ ] Develop MobileApp
	* [ ] Login
	* [ ] Call

## Implementation:
![pic01.png](pic01.png)
 

## Note:
* Secure Copy
	scp your_username@remotehost.edu:/some/remote/directory/\{a,b,c\}

* Show Common Name in Cert
	openssl x509 -noout -subject -in server.pem

* MQTT cmd
	
	sudo systemctl restart mosquitto

	mosquitto_pub -h host -p 8883 --cafile ca.crt -u "user" -P "pwd" -i "client"  -t "test" -m "msg" --tls-version tlsv1
	
	mosquitto_sub -h host -p 8883 --cafile ca.crt -u "user" -P "pwd" -i "client" --tls-version tlsv1 -t "test"
	

## Tutorial:
* Install Mosquitto on Ubuntu

	https://www.digitalocean.com/community/questions/how-to-setup-a-mosquitto-mqtt-server-and-receive-data-from-owntracks

* Setup Secure MQTT Broker

	http://www.steves-internet-guide.com/mosquitto-tls/
	
	https://primalcortex.wordpress.com/2016/03/31/mqtt-mosquitto-broker-with-ssltls-transport-security/
	
* Script to gen certs
	
	https://github.com/owntracks/tools/blob/master/TLS/generate-CA.sh

* Config Mosquitto
	
	https://mosquitto.org/man/mosquitto-conf-5.html
  
  
