# File Management

One of the most important things you have to stay on top of is a decent file management system.  As an artist you will be developing a portfolio of work that you will extend upon every time you start a new project.  There are times when creatively you will want to start fresh and not start with old templates.  But even then you will quickly start slipping in techniques you have learned through previous projects.  As a graphic artist you will want a large library of both raster and vector graphics.  As a musician, you'll want to gather interesting synthesizers and most likely 'presets' for those synthesizers.  3D artists will want models, textures, scenes, and audio to go with it.  And filmmakers will require all of the above and screenwritings, kitchen sinks, and loads of stuff I'm leaving out.

Where to start?  First make a decision of whether to separate out your media, the problem here is that many of your new still cameras are taking great video, for example my:

https://www.dpreview.com/reviews/panasonic-lumix-dmc-lx100

the issue is that it puts the still pictures in the same folder as the videos, I could separate them out, but why take this extra step?  I say just make a 'Media' folder and place the folders from your camera or other hardware in there, using a naming scheme like this:

2015-08-03-GOPRO

Where the file in the camera was named '100GOPRO' I renamed it to the above with something like this on the command line:

```
mv 100GOPRO `date -I`-GOPRO
```

if you don't like the command line you can use whatever GUI method you prefer (right click and choose renmae, etc).  On choosing a date when there is a range of dates for the associated footage inside the folder,  just choose the last date that media was aquired in the folder, to be consistent.

Now when you look at a long list of the file names they will sort by date quite naturally (notice the modification and create dates might be misleading and not useful for our purposes):
```
ls -lh
total 72K
drwxr-xr-x 2 thoth thoth 4.0K Aug 29 14:10 2015-07-22-GOPRO
drwxr-xr-x 2 thoth thoth 4.0K Aug 29 13:58 2015-08-09-GOPRO
drwxr-xr-x 2 thoth thoth 4.0K Aug 31 00:37 2016-02-01-GOPRO
drwxr-xr-x 2 thoth thoth   82 Aug 31 00:38 2016-02-03-GOPRO
drwxr-xr-x 2 thoth thoth 4.0K Aug 29 14:43 2016-04-17-GOPRO
drwxrwxrwx 2 thoth thoth 4.0K Apr 17 15:26 2016-04-18-GOPRO
drwxr-xr-x 4 thoth thoth   43 Aug 29 14:43 2016-04-18-PANA
drwxrwxrwx 2 thoth thoth  12K Apr 22 21:25 2016-04-23-PANA
drwxrwxrwx 2 thoth thoth  16K May  3 15:46 2016-07-24-PANA
```

### De Duplication

Is a very important exercise in any media acquisition. For this I recommend

#### [FSlint](http://www.pixelbeat.org/fslint/) 


>  FSlint is a utility to find and clean various forms of lint on a filesystem.
 I.E. unwanted or problematic cruft in your files or file names.
 For example, one form of lint it finds is duplicate files.
 It has both GUI and command line modes.



One of the nicest things about it is that it can remove duplicate files while leaving a hardlink in place.  This means you can still access the file in both locations, but it only consumes a single copy of hard drive space, until you edit one, then they fork off again from each other.  Hard and Soft links is one of those concepts people usually don't get difference between,  here's a link if you want to know more:

http://www.kevinslonka.com/files/20080918-Symbolic-and-Hard-Links-Explained.pdf

### Backups

You need to have backups in more than one place, given that you are going to be saving video you'll need a lot of space, the best deal I've found for this is the amazon cloud drive:

https://www.amazon.com/clouddrive/

for $60/year you get unlimited* storage space.  The *caveat is that they bandwidth limit you after 1TB/month (from what I can tell), so with my google fiber I was able to upload a terabyte in one night, but I woke up the next day and all transfers had slowed down from 40MB/s to 60KB/s.  It appears the download portion is completely unlimited (or set so high I have not hit it yet).

### [Rclone](http://rclone.org/)

Rclone is my favorite method for uploading and downloading from the Amazon Cloud Drive, and many other cloud services

> Rclone is a command line program to sync files and directories to and from

*     Google Drive
    Amazon S3
    Openstack Swift / Rackspace cloud files / Memset Memstore
    Dropbox
    Google Cloud Storage
    Amazon Drive
    Microsoft One Drive
    Hubic
    Backblaze B2
    Yandex Disk
    The local filesystem


Features

*     MD5/SHA1 hashes checked at all times for file integrity
    Timestamps preserved on files
    Partial syncs supported on a whole file basis
    Copy mode to just copy new/changed files
    Sync (one way) mode to make a directory identical
    Check mode to check for file hash equality
    Can sync to and from network, eg two different cloud accounts
    Optional encryption (Crypt)
    Optional FUSE mount (rclone mount)





