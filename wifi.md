修改/etc/network/interfaces
加上
iface default inet dhcp
內容如下
auto wlan0
allow-hotplug wlan0
iface wlan0 inet manual
wpa-conf /etc/wpa_supplicant/wpa_supplicant.conf
iface default inet dhcp
查無線基地台
$ sudo iwlist wlan0 scan | grep ESSID
修改/etc/wpa_supplicant/wpa_supplicant.conf
檔底加上
network={
        ssid="_ssid_"
        psk="_password_"
        proto=RSN
        key_mgmt=WPA-PSK
        pairwise=CCMP
        auth_alg=OPEN
}
$ sudo ifdown wlan0
$ sudo ifup wlan0 
出現以下訊息,但仍可以用,要等一下
ioctl[SIOCSIWAP]: Operation not permitted
ioctl[SIOCSIWENCODEEXT]: Invalid argument
ioctl[SIOCSIWENCODEEXT]: Invalid argument
