�ק�/etc/network/interfaces
�[�W
iface default inet dhcp
���e�p�U
auto wlan0
allow-hotplug wlan0
iface wlan0 inet manual
wpa-conf /etc/wpa_supplicant/wpa_supplicant.conf
iface default inet dhcp
�d�L�u��a�x
$ sudo iwlist wlan0 scan | grep ESSID
�ק�/etc/wpa_supplicant/wpa_supplicant.conf
�ɩ��[�W
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
�X�{�H�U�T��,�����i�H��,�n���@�U
ioctl[SIOCSIWAP]: Operation not permitted
ioctl[SIOCSIWENCODEEXT]: Invalid argument
ioctl[SIOCSIWENCODEEXT]: Invalid argument
