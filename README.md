TV-show workflow. Once you download a show in Deluge torrenter, this will follow that show forever, assuming it uses a standard season/episode format, and not YYYYMMDD.

Sorry for hard-coded paths. This needs some work to be general.

Deluge Setup
------------

Run Deluge in client/server model.   
Prefs / Interface / Classic mode OFF.

Download to temp dir and rename on completed.    
Prefs / Downloads / Download to "/tmp/torrents-temp"   
Prefs / Downloads / Move completed to "/data/%downloaded-unsorted"

Enable plugin "execute"   
Prefs / Plugins / execute ON

Add "rename" as completed-hook.   
Prefs / Execute / Event Complete "torrent-rename"

Cron
----

Add `dmsid=NNNNNNNNNNNNNN bin/torrents-get /data/movies-and-television/torrents` to your cron list. Run it about once a day.
