# Orange Pi 2G IOT with Android 4.4 + Debian jessie + python + tensorflow + Intel Movidius Neural Compute Stick

For less than 100$ you will have a cheap and performing AI & IOT devkit

My hardware configuration :

https://fr.aliexpress.com/item/Orange-Pi-2G-IOT-ARM-Cortex-A5-32bit-Support-ubuntu-linux-and-android-mini-PC-Beyond/32802458477.html

https://fr.aliexpress.com/item/3-5inch-Black-color-Touch-Screen-LCD-screen-TFT-Suitable-for-Orange-Pi-2G-IOT-Development/32816194245.html?spm=a2g0w.10010108.1000013.2.670c7975I0eG0w&scm=1007.13339.90158.0&scm_id=1007.13339.90158.0&scm-url=1007.13339.90158.0&pvid=c6d13af3-b407-4e31-9da7-3d9f7ddcc24b&_t=pvid%3Ac6d13af3-b407-4e31-9da7-3d9f7ddcc24b%2Cscm-url%3A1007.13339.90158.0

https://www2.mouser.com/m_new/Intel/intel-movidius-stick/

This tutorial assumes that you already have android rooted armv7 device. 

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
