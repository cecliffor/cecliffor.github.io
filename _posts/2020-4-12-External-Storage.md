---
layout: post
title: External Storage
---

My home media server uses three 4TB external hard drives, all connected to the Pi through a powered USB hub and mounted at:
- /media/Media_1/
- /media/Media_2/
- /media/Media_3/

I use Media_2 to upload content to the drives, by manually disconnecting from the server and connecting to my computer.

After moving files to the drive and reconnecting to the server, I sync everying by with:
`sudo rsync -av /media/Media_2/ /media/Media_1/`
`sudo rsync -av /media/Media_2/ /media/Media_3/`

And make sure everything is reverse synced with:

`sudo rsync -av /media/Media_1/ /media/Media_2/`
`sudo rsync -av /media/Media_3/ /media/Media_2/`
