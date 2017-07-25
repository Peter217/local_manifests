<p align="center">
<img src="http://i.imgur.com/ZDi8Osn.png" > 
</p>


Credits
-------
* [**JDCTeam (Base)**](https://github.com/AOSP-JF-MM)
* [**TeamSubstratum (Theme Engine)**](https://github.com/Substratum)
* [**AospExtended**](https://github.com/AospExtended)

Download the Source
-------------------

Please read the [AOSP building instructions](http://source.android.com/source/index.html) before proceeding.

Create dirs, and install soft, libs
-----------------------------------

    sudo su
    add-apt-repository ppa:openjdk-r/ppa
    apt-get update
    apt-get install bison build-essential curl ccache flex lib32ncurses5-dev lib32z1-dev libesd0-dev libncurses5-dev libsdl1.2-dev libxml2 libxml2-utils lzop pngcrush schedtool squashfs-tools xsltproc zip zlib1g-dev git-core make phablet-tools gperf openjdk-8-jdk
    exit
    
    
Install repo
------------

    mkdir ~/bin
    PATH=~/bin:$PATH
    cd ~/bin
    curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
    chmod a+x ~/bin/repo
    

Create mos folder
----------------------

    mkdir ~/mos
    cd ~/mos
    

GIT config (nickname, e-mail)
-----------------------------

    git config --global user.email "mail@domain.com"
    git config --global user.name  "login"
    

To initialize your local repository use
---------------------------------------

    repo init -u https://github.com/MainstageOS/platform_manifest.git -b aosp-7.1.2
    

Then to sync up:
----------------

    repo sync --force-sync -j8 --current-branch --no-tags --no-clone-bundle --optimized-fetch --force-broken

