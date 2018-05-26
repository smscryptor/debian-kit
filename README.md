# Orange Pi 2G IOT with Android 4.4 + Debian jessie + python + tensorflow + Intel Movidius Neural Compute Stick

## download debian kit then make
$ git clone https://github.com/smscryptor/debian-kit.git

$ cd debian_kit && make

## put the install package on android device
$ adb push debian-kit-1-6.shar /data/local

## run the installation on the device
$ adb root

$ adb shell

$ sh /data/local/debian-kit-1-6.shar

## follow the script instructions to finish the installation but do not andromize

$ sh /data/local/deb/deb

$ apt update

$ apt upgrade

$ apt install python-pip python-dev libusb-1.0 sudo

## install tensorflow 1.7 for python2.7 and tensorflow 1.8 for python3

$ pip install grpcio==1.9.1 pbr funcsigs

$ pip install grpcio==1.9.1 http://ci.tensorflow.org/view/Nightly/job/nightly-pi/lastSuccessfulBuild/artifact/output-artifacts/tensorflow-1.7.0-cp27-none-any.whl

$ pip3 install --upgrade http://ci.tensorflow.org/view/Nightly/job/nightly-pi-python3/lastSuccessfulBuild/artifact/output-artifacts/tensorflow-1.8.0-cp34-none-any.whl


## get the ncs source release V2

https://github.com/smscryptor/ncsdk/tree/ncsdk2

## install the ncsdk

$ make install

# DONE !
