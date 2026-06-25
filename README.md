# TRUENAS<sub>PL</sub>
Polska lokalizacja [Truenas Scale](https://github.com/truenas/) → [Goldeye 25.10.4](https://download.truenas.com/TrueNAS-SCALE-Goldeye/25.10.4/) ▪ WIP ▪ **87%**  
W oparciu o [truenas/.../en.json](https://github.com/truenas/webui/blob/d2fd62021d24de361d27d6af132fb4b80e4c4c46/src/assets/i18n/en.json)

## odblokowujemy system plików
```Shell
sudo /usr/local/libexec/disable-rootfs-protection
```

## kopiujemy spolszczenie

### język ui: pl (wersja stabilna)

```Shell
wget -O pl.json https://raw.githubusercontent.com/warchlak/truenaspl/refs/heads/main/pl.json; sudo cp pl.json /usr/share/truenas/webui/assets/i18n/pl.json; sudo service nginx restart; sudo service middlewared restart
```

### język ui: en (wersja nightly)

```sh
wget -O pl.json https://raw.githubusercontent.com/warchlak/truenaspl/refs/heads/main/pl.json; sudo cp pl.json /usr/share/truenas/webui/assets/i18n/en.json; sudo service nginx restart; sudo service middlewared restart
```
