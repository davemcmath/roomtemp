# roomtemp

sudo apt-get update && sudo apt-get upgrade -y

sudo rpi-update

sudo reboot

sudo raspi-config

Enable -  SPI, I2C and 1-Wire

sudo apt-get update

sudo apt-get install build-essential python-dev python-openssl python-influxdb -y

scp pi@192.168.66.72:/home/pi/Adafruit_Python_DHT.tgz /home/pi

scp pi@192.168.66.72:/home/pi/*.py /home/pi/

tar -xvf Adafruit_Python_DHT.tgz

sudo python setup.py install

sudo python Adafruit_Python_DHT/examples/AdafruitDHT.py 22 4
