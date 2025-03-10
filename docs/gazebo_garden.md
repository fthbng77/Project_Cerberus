### Uyarı: Sisteminde gazebo 11 yüklü olanlarda hata çıkabilir.
WARNING: for gazebo-classic (eg. `gazebo11`) users: `gz-garden` cannot be installed alongside with `gazebo11` by default. To facilitate the migration this can be done using the instruction detailed in Installing [Gazebo11 side by side with new Gazebo](https://gazebosim.org/docs/garden/install_gz11_side_by_side/)

Önce aşağıdaki işlemleri tamamlayın:
```
sudo add-apt-repository ppa:openrobotics/gazebo11-gz-cli
sudo apt update
sudo apt-get install gazebo11
```

## Instal Gazebo Sim (Garden) 
```
sudo apt-get update
sudo apt-get install lsb-release curl gnupg
```
```
sudo curl https://packages.osrfoundation.org/gazebo.gpg --output /usr/share/keyrings/pkgs-osrf-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/pkgs-osrf-archive-keyring.gpg] http://packages.osrfoundation.org/gazebo/ubuntu-stable $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/gazebo-stable.list > /dev/null
sudo apt-get update
sudo apt-get install gz-garden
```

