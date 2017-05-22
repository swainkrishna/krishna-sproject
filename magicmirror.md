#!/bin/bash  
MACHINE_TYPE=`uname -m`
	if [ ${MACHINE_TYPE} == 'x86_64' ]; then
		  echo "this device is 64bit"
                  echo "DOWNLOADING NODE.JS ..."
		  wget  https://nodejs.org/dist/v6.10.3/node-v6.10.3-linux-x86.tar.xz
                  echo "INSTALLING NODE.JS ..."
		  wget    https://deb.nodesource.com/setup_6.x | sudo -E bash -
		  sudo apt-get install -y nodejs
                  echo "INSTALLATION SUCCESSFUL!!!"


	else
		  echo "this device is 32bit"
		  echo "DOWNLOADING NODE.JS ..."
		  wget  https://nodejs.org/dist/v6.10.3/node-v6.10.3-linux-x64.tar.xz
		  echo "INSTALLING NODE.JS ..."
		  wget    https://deb.nodesource.com/setup_6.x | sudo -E bash -
		  sudo apt-get install -y nodejs
		  echo "INSTALLATION SUCCESSFUL!!!"
	fi
git clone https://github.com/MichMich/MagicMirror
cd ~/MagicMirror
npm install 
npm start
