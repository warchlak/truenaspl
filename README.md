# TRUENAS<sub>PL</sub>
Polska lokalizacja [Truenas Scale](https://github.com/truenas/) → [Fangtooth](https://download.truenas.com/TrueNAS-SCALE-Fangtooth/25.04.0/?wrap=1) ▪ WIP ▪ **33%**  
W oparciu o [truenas/.../en.json](https://github.com/truenas/webui/blob/d2fd62021d24de361d27d6af132fb4b80e4c4c46/src/assets/i18n/en.json)

## odblokowujemy system plików
```Shell
sudo /usr/local/libexec/disable-rootfs-protection
```

## kopiujemy spolszczenie

### język ui: pl (wersja stabilna)

```Shell
wget -O en.json https://raw.githubusercontent.com/warchlak/truenaspl/refs/heads/main/en.json; sudo cp en.json /usr/share/truenas/webui/assets/i18n/pl.json; sudo service nginx restart; sudo service middlewared restart
```

### język ui: en (wersja nightly)

```sh
wget -O en.json https://raw.githubusercontent.com/warchlak/truenaspl/refs/heads/main/en.json; sudo cp en.json /usr/share/truenas/webui/assets/i18n/; sudo service nginx restart; sudo service middlewared restart
```
