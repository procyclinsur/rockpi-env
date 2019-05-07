# rockpi-env
Debian Environment Changes for the Rock Pi 4B

## Install MATE Desktop
```bash
sudo apt update
sudo apt -y install 
              task-mate-desktop \
              mate-desktop-environment-extras \
              blueman \
              caja-gksu \
              caja-image-converter \
              caja-open-terminal \
              caja-sendto \
              caja-share \
              caja-wallpaper \
              dconf-editor \
              mate-sensors-applet \
              mate-user-share \
              mozo \
              yelp \
              im-config \
              ibus-anthy \
              kasumi \
              task-japanese \
              locales-all
              
sudo update-alternatives --install /usr/bin/x-session-manager x-session-manager /usr/bin/mate-session 100
sudo update-alternatives --install /usr/bin/x-window-manager x-window-manager /usr/bin/marco 100

# CREATE NEW USER

# DISABLE AUTO-LOGIN FOR DEFAULT USER
sudo sed -i "s/autologin-user=linaro/#autologin-user=linaro/" /etc/lightdm/lightdm.conf
sudo sed -i "s/autologin-user-timeout=0/#autologin-user-timeout=0/" /etc/lightdm/lightdm.conf

sudo reboot
```
