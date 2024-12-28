# TRUENAS<sub>PL</sub>
Polska lokalizacja [Truenas Scale](https://github.com/truenas/) -- [ElectricEel-24.10.1](https://download.truenas.com/TrueNAS-SCALE-ElectricEel/24.10.1/) -- WIP -- **35%**

## odblokowujemy system plików
```Shell
sudo /usr/local/libexec/disable-rootfs-protection
```

## kopiujemy spolszczenie

### wersja stabilna, język ui - pl
```Shell
sudo cp /mnt/ścieżka-do-tego-pliku/en.json /usr/share/truenas/webui/assets/i18n/pl.json
```
lub aio
```Shell
wget https://raw.githubusercontent.com/warchlak/truenaspl/refs/heads/main/en.json; sudo cp en.json /usr/share/truenas/webui/assets/i18n/pl.json; sudo service nginx restart; sudo service middlewared restart
```

### wersja nightly, język ui - en
```sh
sudo cp /mnt/ścieżka-do-tego-pliku/en.json /usr/share/truenas/webui/assets/i18n/
```
lub aio
```sh
wget https://raw.githubusercontent.com/warchlak/truenaspl/refs/heads/main/en.json; sudo cp en.json /usr/share/truenas/webui/assets/i18n/; sudo service nginx restart; sudo service middlewared restart
```

### obie wersje, restartujemy usługi
```sh
sudo service nginx restart
sudo service middlewared restart
```
