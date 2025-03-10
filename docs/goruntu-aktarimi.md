## ROS2 Kullanılarak Görüntü Aktarımı

### USB-cam ROS2 paketinin kurulması

Aşağıdaki komutla usb-cam paketi kurulur.
```
sudo apt-get install ros-humble-usb-cam
```
image tools paketi kurulumu:
```
sudo apt install ros-humble-image-tools
```

### Bilgisayarlar arası bağlantının kurulması

Ros2 ile görüntü aktarımı yapmak için bilgisayarların aynı wi-fi ağına bağlanması sağlanmalı. 

Ardından iki bilgisayarda da .bashrc'ye aşağıdaki satır eklenerek iki bilgisayarın aynı ROS DomainID üzerinden haberleşmesi sağlanmalı.
```
export ROS_DOMAIN_ID=30
```
Burada 30 rastgele bir sayıdır dikkat edilmesi gereken iki bilgisayarda da aynı sayının yazılması ve aynı wi-fi üzerinde aynı domain id ile haberleşen başka ros sisteminin olmamasıdır.

**ROS DomainID:** Domain ID, aynı ağ üzerinde çalışan ROS2 düğümlerinin (nodes) birbirleriyle haberleşme sınırlarını tanımlar. Sadece aynı Domain ID'ye sahip düğümler birbiriyle iletişim kurabilir. Bu, ağ üzerinde birden fazla ROS2 uygulamasının bağımsız olarak çalışmasını sağlar ve mesajlaşma çakışmalarını önler.

## usb-cam node'unun başlatışması ve tpicleri görüntülemek için komutlar:

Aşağıdaki node ile usb-cam başlatılır
```
ros2 run usb_cam usb_cam_node_exe
```

NOT: Camera parametrelerini ayarlayıp bir .yaml dosyası ile çalıştırmak için yukarıdaki komut aşağıdaki gibi güncellenerek kullanılmalı:
```
ros2 run usb_cam usb_cam_node_exe --ros-args --params-file colcon_ws/src/usb_cam/config/params.yaml
```

#### Alıcı bilgisayarda:

Topicleri görüntülemek ve yayınlamak için:
```
ros2 topic list
```

```
ros2 topic echo /image_raw
```

```
rqt
```


