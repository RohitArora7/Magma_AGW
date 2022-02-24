# Magma_AGW

```bash
su
wget https://raw.githubusercontent.com/magma/magma/v1.6/lte/gateway/deploy/agw_install_ubuntu.sh
bash agw_install_ubuntu.sh 192.168.5.120/24 192.168.5.1
```


```bash
find / -name "magma" -type d

/usr/local/lib/python3.8/dist-packages/magma
/usr/local/share/magma
/usr/share/doc/magma

/var/opt/magma
/home/magma
/etc/magma

```

```bash
service magma@* stop
service magma@magmad start
sudo service magma@* status

sudo netstat -l | grep sctp 
cat /proc/net/sctp/eps
sudo tail -f /var/log/mme.log
journalctl -fu magma@magmad

```

```bash
cd /var/opt/magma/tmp

    TAI_LIST = (

         { MCC="001" ; MNC="01" ; TAC="1"; }
    );

    TAC_LIST = (
         { MCC="001" ; MNC="01" ; TAC="1"; }

    );
```

```bash
sudo rm /var/opt/magma/certs/gateway.crt
sudo rm /var/opt/magma/certs/gateway.key
sudo rm /var/opt/magma/configs/gateway.mconfig
```

```bash
sudo cp mme_binary /usr/local/bin/
sudo mv mme mme.bak
sudo mv mme_binary mme
sudo service magma@mme stop
sudo service magma@mme restart
```

