# UNSUPPORTED

This project is no longer being developed. If someone would like to take it over please open an issue to let me know.

# Python QBittorrent Client

A simple python class to interface with QBittorrent. Currently only supporst the 3.1.x version of the API.

For more details on the web api visit https://github.com/qbittorrent/qBittorrent/wiki/WebUI-API-Documentation-%28qBittorrent-v3.1.x%29

## Installation

```
$ pip install qbittorrent
```

## Example

```python
from qbittorent import Client

qb = Client(url='http://localhost:8080') qb.login('admin', 'secret')

torrents = qb.torrents()

for torrent in torrents:
   print(torrent['name'])

```

## API

class qbittorrent.client.Client(url)

   addTrackers(hash, trackers)

      Add trackers to torrent

      trackers can be a string or a list

   bottomPrio(hashes)

      Minimal torrent priority

      hashes could be a string or a list

   decreasePrio(hashes)

      Decrease torrent priority

      hashes could be a string or a list

   delete(hashes)

      Delete torrent

      hashes can be a string or a list

   deletePerm(hashes)

      Delete torrent with download data

      hashes could be a string or a list

   download(urls)

      Download torrent from URL

      Pass list of URLs as a list

   getGlobalDlLimit()

      Get global download limit

   getGlobalUpLimit()

      Get global upload limit

   getTorrentDlLimit(hash)

      Get torrent download limit

   getTorrentUpLimit(hash)

      Get torrent upload limit

   increasePrio(hashes)

      Increase torrent priority

      hashes could be a string or a list

   login(username, password)

      Login

      Arguments: username -- username password -- password

   pause(hash)

      Pause torrent

   pauseAll()

      Pause all torrents

   preferences()

      Get qBittorrent preferences

   propertiesFiles(hash)

      Get torrent contents

   propertiesGeneral(hash)

      Get torrent generic properties

   propertiesTrackers(hash)

      Get torrent trackers

   recheck(hashes)

      Recheck torrent

      hashes could be a string or a list

   resume(hash)

      Resume torrent

   resumeAll()

      Resume all torrents

   setFilePrio(hash, id, priority)

      Set file priority

   setGlobalDlLimit(limit)

      Set global download limit

   setGlobalUpLimit(limit)

      Set global upload limit

   setPreferences(**kwargs)

      Set preferences

   setTorrentDlLimit(hash, limit)

      Set torrent download limit

   setTorrentUpLimit(hash, limit)

      Set torrent download limit

   topPrio(hashes)

      Maximal torrent priority

      hashes could be a string or a list

   torrents()

      Get torrent list

   transerInfo()

      Get global transfer info
