# python-qbittorrent
Python wrapper to the QBittorrent web api. Currently only supports the v3.1.x of the API.

Refer to https://github.com/qbittorrent/qBittorrent/wiki/WebUI-API-Documentation-%28qBittorrent-v3.1.x%29 for a list of API commands.

## example

```python
qb = QBittorrent(url='http://localhost:8080')

qb.login('admin', 'admin')

torrents = qb.torrents()

for torrent in torrents:
  print torrent['name']
```

## api



Refer to https://github.com/qbittorrent/qBittorrent/wiki/WebUI-API-Documentation-%28qBittorrent-v3.1.x%29 for a list of API commands.
