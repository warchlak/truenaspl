# TRUENAS<sub>PL</sub>
Polska lokalizacja [Truenas Scale](https://github.com/truenas/) -- [Fangtooth](https://download.truenas.com/TrueNAS-SCALE-Fangtooth/25.04.0/?wrap=1) -- WIP -- **33%**

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
