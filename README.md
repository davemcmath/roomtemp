# roomtemp

	sudo apt-get update && sudo apt-get upgrade -y

	sudo rpi-update

	sudo reboot

	sudo raspi-config

Enable -  SPI, I2C and 1-Wire

	sudo apt-get update

	sudo apt-get install build-essential python-dev python-openssl python-influxdb -y


Pull Adafruit Library for DHT22
	scp pi@<working IP Temp Pi>:/home/pi/Adafruit_Python_DHT.tgz /home/pi
Pull Python scripts from working Pi
	scp pi@<working IP Temp Pi>:/home/pi/*.py /home/pi/
Pull restart script from working Pi
	scp pi@<working IP Temp Pi>3:/home/pi/*.sh /home/pi/



	tar -xvf Adafruit_Python_DHT.tgz

	sudo python setup.py install

	sudo python Adafruit_Python_DHT/examples/AdafruitDHT.py 22 4


	#!/bin/bash
	cronline1="5 * * * * /home/pi/restartscript.sh"
	cronline2="@reboot /home/pi/restartscript.sh"
	(crontab -u pi -l; echo "$cronline1" ) | crontab -u pi -
	(crontab -u pi -l; echo "$cronline2" ) | crontab -u pi -
	crontab -l
