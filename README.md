# version 1.0	initial version  Decemeber 2017

Copyright (c) 2017 Paul van Haastrecht <paulvha@hotmail.com>


## Background
As part of a larger project I am looking at analyzing and understanding the air quality. 
The aim of this project was to better understand the kind of gas-types that are in the air. 

I have ported the library to CPP on a Raspberry PI running Raspbian Jessie release. It has been 
adjusted and extended for stable working.

Getting the CCS811 working stable on i2C was a big challenge, as explained in more detail in the 
combo.odt.

As I also own a Dylos DC1700, I have included the driver in this program and run measurments 
in parallel to compare the results. Interesting enough the TVOC values are close to the PM10 
results from the Dylos

For detailed information about findings, the hardware and software, please read the included combo.odt
 
## Software installation

Make your self superuser : sudo bash

BCM2835 library
Install latest from BCM2835 from : http://www.airspayce.com/mikem/bcm2835/

1. cd /home/pi
2. wget http://www.airspayce.com/mikem/bcm2835/bcm2835-1.52.tar.gz
3. tar -zxf bcm2835-1.52.tar.gz		// 1.52 was version number at the time of writing
4. cd bcm2835-1.52
5. ./configure
6. sudo make check
7. sudo make install

Installation of Combo software :

1. cd /home/pi
2. tar -zxf combo-1.tar.gz
3. cd combo
4. create the executable : make  
5. To run you have to be as root : sudo ./combo 

To get help : ./combo -h

(detailed description of the many options in  combo.odt)

