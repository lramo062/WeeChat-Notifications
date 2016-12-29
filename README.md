# WeeChat-Notifications
WeeChat-Notificatoins is a plugin for WeeChat, a CLI chat client on linux with i3-wm instructions.

* Forked from https://github.com/omart075/WeeNotifyMatrix.
* WeeChat-Notifications displays a notification whenever a message is received on any buffer you have on WeeChat.
* Uses dunst & notify-send to display notifications.


![Alt text](/weeNotifyPic.png?raw=true "Script in Action")

# Instructions for Use:
  1. Make sure you have the following installed:
      * [WeeChat](https://weechat.org/)
      * [Matrix](https://github.com/torhve/weechat-matrix-protocol-script/blob/master/README.md) 
      * [Dunst](https://github.com/knopwob/dunst)
      
  2. Clone this repo:
  ```     
    git clone https://github.com/lramo062/WeeChat-Notifications/  
  ``` 
  3. Move script to WeeChat's Python Directory:
  
  ```
    mv weeNotify.py ~/.weechat/python
  ```  
  4. Go into WeeChat's autoload directory for Python:
  
  ```
    cd ~/.weechat/python/autoload
  ```  
  5. Make a link to script from Weechat's Python dir to WeeChat's autoload dir:
  
  ```
    ln -s ../weeNotify.py
  ```
   6. Add the dunstrc file to correct path
  
  ```
    cp dunstrc /usr/share/dunstrc
  ```
  7. For i3-wm users you will need to add the following to your config file:
  
  ```
    exec --no-startup-id dunst -config /usr/share/dunst/dunstrc
  ```  
