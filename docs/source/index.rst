# Python QBittorrent Client

A simple python class to interface with QBittorrent. Currently only supporst the 3.1.x version of the API.

For more details on the web api visit https://github.com/qbittorrent/qBittorrent/wiki/WebUI-API-Documentation-%28qBittorrent-v3.1.x%29

## Example

```python
from qbittorent.client import Client

qb = Client(url='http://localhost:8080')
qb.login('admin', 'secret')

torrents = qb.torrents()

for torrent in torrents:
  print(torrent['name'])
```

## API

.. autoclass:: qbittorrent.client.Client
   :members:


