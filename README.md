# truenaspl
Polska lokalizacja [Truenas Scale](https://github.com/truenas/) -- [ElectricEel-24.10.1](https://download.truenas.com/TrueNAS-SCALE-ElectricEel/24.10.1/) -- WIP

## odblokowujemy system plików
```
sudo /usr/local/libexec/disable-rootfs-protection
```

## kopiujemy spolszczenie

### wersja stabilna, język ui - pl
```
sudo cp /mnt/ścieżka-do-tego-pliku/en.json /usr/share/truenas/webui/assets/i18n/pl.json
```
lub aio
```
wget https://raw.githubusercontent.com/warchlak/truenaspl/refs/heads/main/en.json; sudo cp en.json /usr/share/truenas/webui/assets/i18n/pl.json; sudo service nginx restart; sudo service middlewared restart
```

### wersja nightly, język ui - en
```
sudo cp /mnt/ścieżka-do-tego-pliku/en.json /usr/share/truenas/webui/assets/i18n/
```
lub aio
```
wget https://raw.githubusercontent.com/warchlak/truenaspl/refs/heads/main/en.json; sudo cp en.json /usr/share/truenas/webui/assets/i18n/; sudo service nginx restart; sudo service middlewared restart
```

### obie wersje, restartujemy usługi
```
sudo service nginx restart
sudo service middlewared restart
```
