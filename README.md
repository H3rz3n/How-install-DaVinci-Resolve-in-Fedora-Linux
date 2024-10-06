# How install DaVinci Resolve in Fedora Linux

<p align="center">
  <img src="/Banne.png" alt="Banner"/>
</p>

DaVinci Resolve is one of the most popular video editing software and, unlike Adobe Premiere, it supports Linux with a native application. By default, DaVinci Resolve officially supports only the Rocky Linux distribution, but with some tricks it's possible to install it in other distrution of the RHEL family, like Fedora Linux.  

In this guide will be covered the download and the installation of DaVinci Resolve on Fedora Linux using DaVinci Helper, an app I developed to make this process easier for the Linux novice users.

## How download DaVinci Resolve
The most simple and secure way to download DaVinci Resolve is from the [manufacter's website](https://www.blackmagicdesign.com/it/products/davinciresolve/).  
Before downloading let's see the download options that you have :
- **DaVinci Resolve Studio :** The Studio version has all the features of DaVinci Resolve Free but with some additional effects, codecs support and the support for multiple GPU transcoding and NVENC transcoding.
- **DaVinci Resolve Free :** The Free version is the complete version of DaVinci Resolve that does not require any license, but lacks of the support of common codecs like AAC and H264/H265 (used by most cameras and smartphone) requiring to convert the videos and audios in one of the few supported codecs.

Regardless of the version you selected you need to download the corresponding Linux version. To complete the download you need to compile a small form, *but you can write there fake data if you don't want to give too much information to BlackmagicDesign*.  

Personally, I would recommend you trying the Free version and buying the Studio version in case it corresponds to your needs. The software is really good and it's a good way to support BlackMagic Design to keep developing the Linux version.



## How install DaVinci Helper in Fedora 40-41
The most simple way to install and keep [DaVinci Helper](https://github.com/H3rz3n/davinci-helper) updated is by adding the project COPR repository to your repository list and simply install it with the DNF packet manager.

### Adding the project COPR repository
Open a terminal window and paste this instruction : 
```
sudo dnf copr enable -y herzen/davinci-helper
```

### Installing the app
Open a terminal window and paste this instruction :  
```
sudo dnf install -y davinci-helper
```


## How use DaVinci Helper to correctly install and patch DaVinci Resolve
Now that you have DaVinci Resolve and the right tool to assist use, let's open DaVinci Helper. 

### Prepare the system
You need to start from the first section of Davinci Helper called `Install missing dependencies` and click the start button to launch the dependecies check.

<p align="center">
  <img src="https://github.com/H3rz3n/davinci-helper/blob/main/screenshot/02.png?raw=true" alt="Banner"/>
</p>

### Install DaVinci Resolve
If the procedure ends without any errors you can now proceed to install DaVinci Resolve. The DaVinci Resolve installer file you downloaded previously needs to be started with some flags to correcly launch in Fedora Linux.  
The easiest way to do that is to use the second section of DaVinci Helper called `Launch DaVinci Resolve installer`. You need to load the `.zip` file downloaded and then click the start button to launch the DaVinci Resolve installation wizard.

<p align="center">
  <img src="https://github.com/H3rz3n/davinci-helper/blob/main/screenshot/03.png?raw=true" alt="Banner"/>
</p>

### Apply the necessary post installation fix
After you completed the installation you need to move in a secure folder some problematic libraries that DaVinci installs because they will cause errors during the DaVinci Resolve start up. Let's go on the third section of Davinci Helper called `Apply post installation fix` and click the start button to fix the DaVinci Resolve dependecies folder.

<p align="center">
  <img src="https://github.com/H3rz3n/davinci-helper/blob/main/screenshot/04.png?raw=true" alt="Banner"/>
</p>

### Optional : Check the GPU drivers and if the GPU is supported
If the procedure ends without any errors you have finished to install DaVinci Resolve, but if you are not certain if you are using the correct GPU drivers or if your GPU is supported by DaVinci Resolve, you can go to the fourth section of Davinci Helper called `Check and install GPU drivers` and click the start button to check that.

<p align="center">
  <img src="https://github.com/H3rz3n/davinci-helper/blob/main/screenshot/05.png?raw=true" alt="Banner"/>
</p>

### Optional : Easily convert your video for DaVinci Resolve Free
The only problem of DaVinci Resolve Free on Linux is his lack of supports for common codecs like H264/H265 and AAC due to licensing problems. The most simple way to make your videos compatible with DaVinci Resolve Free is to use the fifth section of Davinci Helper called `DaVinci Video Converter`.  
It's a video simple video converter based on FFMPEG and Moviepy that will allow you to use simple (but complete) settings to convert your files in a format compatible with DaVinci Resolve Free.

<p align="center">
  <img src="https://github.com/H3rz3n/davinci-helper/blob/main/screenshot/06.png?raw=true" alt="Banner"/>
</p>

It's very easy to use, just click the load files button to load your sources, select an output folder and the output settings that fits more your usecase and launch the conversion.

## What you can do to contribute to DaVinci Helper development ?
If you want to contribute to the development of [DaVinci Helper](https://github.com/H3rz3n/davinci-helper) you can help us [testing the GPU drivers](https://github.com/H3rz3n/davinci-helper/discussions), translating the app or [making a donation](https://www.paypal.com/donate/?hosted_button_id=CPCG2RFAV82T8) to support the work needed for the maintenance and the continue update to keep up with the latest DaVinci and Fedora versions.
