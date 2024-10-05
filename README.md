# How install DaVinci Resolve in Fedora Linux
DaVinci Resolve is one of the post popular video editing software and, unlike Adobe Premiere, it supports Linux with a native application. By default, DaVinci Resolve officially supports only the Rocky Linux distribution, but with some tricks is possible to install it in other distrution of the RHEL family, like Fedora Linux.  

In this guide we will cover the download and the installation of DaVinci Resolve on Fedora Linux using DaVinci Helper, an app I developed to make this process easier for the Linux novice users.

## How download DaVinci Resolve
The most simple and secure way to donwload DaVinci Resolve is from the [manufacter's website](https://www.blackmagicdesign.com/it/products/davinciresolve/).  
Before downloading let's see the download options that we have :
- **DaVinci Resolve Studio :** The Studio version all the features of DaVinci Resolve Free but with some additional effects, codecs support and the support for multiple GPU transcoding and NVENC transcoding.
- **DaVinci Resolve Free :** The Free version is the complete version DaVinci Resolve that does not require any license, but lacks of the support of the exclusive features of the Studio version.

Regardless of the version we selected we need to donwload the corresponding Linux version. To complete the download we need to compile a small form, *but we can write here fake datas if we don't want to give to much information to BlackmagicDesign*.  

Personally I recommend you to try the Free version and if it suits you to buy the Studio version. Thw software is really good and it's a good way to support BlackMagic Design to keep developing the Linux version.



## How install DaVinci Helper in Fedora 40-41
The most simple way to install and keep [DaVinci Helper](https://github.com/H3rz3n/davinci-helper) updated is to add the project COPR repository to your repository list and simply install it with the DNF packet manager.

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
Now that we have DaVinci Resolve and the right tool to assist use, let's open DaVinci Helper. We need to start from the first section `Install missing dependencies` and click the start button to launch the dependecies check.
<p align="center">
  <img src="https://github.com/H3rz3n/davinci-helper/blob/main/screenshot/02.png?raw=true" alt="Banner"/>
</p>


#
