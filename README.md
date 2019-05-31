# Labsensing

## Directories:

### Components:
  Just the bare minimum.
  
### Nodes:
  Actual implementations being used in our network.
  
### Scripts:
  Installation and useful commands.

#### Computer Nodes:
  Scripts to install and configure regular transmissions on regular machines (tested on Debian 9).

### Data:
  Just being used to fetch data from the server (which is positioned behind a firewall) without having to use multiple SCP commands.

### Flows:
  Every new flow added to the current implementation will be put in this directory. 


#### Main flow used:
![Main Flow Used](images/flow.png?raw=true "Main flow used.")


### Dependencies and Configuration Files:
  The global functions written for this system are kept in a separate repository to facilitate development on Windows and Linux. This is because the Arduino software is very picky about where you keep your libraries. This way you can clone this repository to your Arduino directory and clone the dependencies into your Arduino libraries' directory. The repository is https://github.com/kaylani2/labsensingDependencies.
  The system also uses third party libraries, all of these can be installed with the library manager in the Arduino software. Every other dependency will be listed in this section with the associated download link and date.

### Note on Security:
  None of the installation scripts are configuring secure connections (SSL/TLS). These options are available for Mosquitto, Node-RED and InfluxDB, but the ESP8266 has a hard time with that. That means that the credentials sent from the ESP8266 modules are in plain text, be aware of this when positioning your network.
  Secure connections are being developed for other microcontrollers and will be added when they are tested and implemented on Labsensing.
