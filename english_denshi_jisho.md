English Denshi Jisho Project
============================

Hardware
--------

  1. Computer
    * RPI 4 Model B
  2. Display
    * Osoyonoo 5in RPI DSPI display Capacitive Touch V2.0
    * Resolution 800x480

Software
--------
  1. OS
    * DietPI 64bit
  2. Jisho package
    * Python scripts
    * Display with Tkinter
    * What kind of options do I want to have?

Ideas to Incorporate
--------------------
  * [Sleep mode for DietPI](https://dietpi.com/phpbb/viewtopic.php?t=6928)

Journal
-------  

### 2021.05.31
  * Created hello world test script
  * Tkinter
    * Works in X
    * Does not work without X
  * Launch of X is as fast as terminal only, so maybe no compromise
  * Japanese worked on desktop pi, need to check for dietpi
    * Did not work directly on dietpi
    * Try: install ibus-mozc
      * Can use mozc, but still cannot see Japanese
      * Just noticed locale was still set to C-utf-8, changed to en-utf-8
        * NG
      * installed fonts-takao-gothic
      * Added the following to `$HOME/.bashrc`
  * Gave up on DietPi, moving to RaspiLite
  * Install
    * sudo apt install -y --no-install-recommends xserver-xorg-core xserver-xorg xfonts-base xinit
    * sudo apt install -y --no-install-recommends xfce4 desktop-base lightdm
    * sudo apt install -y --no-install-recommends xfce4-terminal mousepad file-roller thunar-volman network-manager xfce-taskmanager xfce4-notifyd xpdf 
  * Japanese input
    * Modified /etc/locale.gen
      * Uncomment en_US.UTF-8 UTF-8
      * Uncomment ja_JP.UTF-8 UTF-8
   * im-config
         `export GTK_IM_MODULE=ibus`
         `export XMODIFIERS=@IM=IBUS`
         `export QT_IM_MODULE=ibus`
