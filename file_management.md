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

### De Duplication

Is a very important exercise in any media acquisition. For this I recommend

#### [FSlint](http://www.pixelbeat.org/fslint/) 

###### FSlint is a utility to find and clean various forms of lint on a filesystem.
###### I.E. unwanted or problematic cruft in your files or file names.
###### For example, one form of lint it finds is duplicate files.
###### It has both GUI and command line modes.

One of the nicest things about it is that it can remove duplicate files while leaving a hardlink in place.  This means you can still access the file in both locations, but it only consumes a single copy of hard drive space, until you edit one, then they fork off again from each other.  Hard and Soft links is one of those concepts people usually don't get difference between,  here's a link if you want to know more:

http://www.kevinslonka.com/files/20080918-Symbolic-and-Hard-Links-Explained.pdf

