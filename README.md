<h1 align="center">
  <img src="public/Openwrt_logo_square.png" width="200">
        <br>
    SDK Open-WRT
</h1>
<p>how to use the Openwrt SDK compiler correctly</p>
<br>

## Prerequisites :  
- Open-WRT image builder SDK. 
- PC linux.

## Install required dependencies :
```
sudo apt update
```
```
sudo apt install build-essential ccache ecj fastjar file g++ gawk \
gettext git java-propose-classpath libelf-dev libncurses5-dev \
libncursesw5-dev libssl-dev python python2.7-dev python3 unzip wget \
python3-distutils python3-setuptools rsync subversion swig time \
xsltproc zlib1g-dev
```
## Clone SKD repository
```
git clone https://github.com/igorpopovicz/Openwrt-SKD.git
```
## Update and install feeds
```
./scripts/feeds update -a

./scripts/feeds install -a

```
## Configure target and options
```
make menuconfig

```
## Compile the image
```
make -j12 | make -j12 V=s
```
<br>

 <strong>
to preset the firmware settings :
  </strong>
   <br>
    You can include custom files in your image by placing them in |base|/files, e.g. if you want to have my_config included in your image in the directory /etc/config/ ⇒ |base|/files/etc/config/my_config. If the files directory doesn't exist on your buildsystem, then create it.
      <br>
        <br>

<strong>
* Images in /bin/targets/ramips/mt76x8 (if it is mt7688)
 </strong>
   <br>
      <strong>
       * squashfs-sysupgrade used when already have a firmware version  
        </strong>
         <br>
          <strong>
           * initramfs-kernel for flash firmware in boot-loader        
            </strong>


  <br>
    <br>
























 by Popovicz. ͡•_ゝ ͡•




