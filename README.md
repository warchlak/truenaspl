# truenaspl
Polska lokalizacja Truenas Scale - WIP

### wersja stabilna, język ui - pl
```
sudo cp /mnt/ścieżka-do-tego-pliku/en.json /usr/share/truenas/webui/assets/i18n/pl.json
```

### wersja nightly, język ui - en
Odblokowanie fs
```
sudo /usr/local/libexec/disable-rootfs-protection
```

Kopiujemy spolszczenie
```
sudo cp /mnt/ścieżka-do-tego-pliku/en.json /usr/share/truenas/webui/assets/i18n/
```

### obie wersje, restartujemy usługi
```
sudo service nginx restart
sudo service middlewared restart
```
