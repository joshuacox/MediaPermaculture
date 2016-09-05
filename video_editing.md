# Video Editing

### [Kdenlive](https://kdenlive.org/)


> Kdenlive is an acronym for KDE Non-Linear Video Editor. It is primarily aimed at the GNU/Linux platform but also works on BSD and MacOS. It is currently being ported to Windows as a GSOC project.
Non-linear video editing is much more powerful than beginners’ (linear) editors, hence it requires a bit more organization before starting. However, it is not reserved to specialists and can be used for small personal projects.



Excellent tutorial introducing offline editing [Seth Kenlon](https://opensource.com/life/16/1/offline-editing-kdenlive)

### [Easy-logging](http://easy-logging.net/)


> Easy-logging 2.0 is an addon that offers de-rushing and tagging functionnalities to the Blender video sequence editor.



## miniDV


> If you have any minicam footage from the aughties (2000s), it is most likely on a miniDV tape, you might also have found that it is notoriously difficult to capture these tapes to hard drive (especially in the early days).  The computer hiccup while encoding the stream coming from the tape and there would be a burp in the captured footage, and you would have to do this over and over till the gods deemed you worthy and let the thing capture properly.  Well, along came linux, and by foregoing the necessity to also draw the footage coming into the computer on the screen at the same time, I could finally reliably capture miniDV footage on a cheap second hand laptop, whereas my $3,000 dollar Macintosh was still struggling.  And apple claims to have invented 'firewire'.  So if you happen to have some miniDV tapes laying around that need to be captured before the magnetic material start flaking off the tape, then read on.



### [Kino](http://kinodv.org/)

While they have this to say:


> Kino has not been actively maintained since 2009. We encourage you to try other Linux video editors such as Shotcut, Kdenlive, Flowblade, OpenShot, PiTiVi, LiVES, and LightWorks.



They did give us another great project:

#### dvgrab

This is the backend that kino uses to capture video, but if you forego using kino and use this command line utility you'll get amazing capture results.  As I stated earlier, because dvgrab does not attempt to display the incoming stream I have never seen it fail.  This is in stark contrast to my experience on the Macintosh, where I would say a significant portion of all captures would fail consistently.

Here is the command I most often use:

```
dvgrab -autosplit -timestamp foo-
```

it will autosplit when it detects a new clip (the camera stops), and will name the resulting file 'foo-' with a timestamp from the timecode given by the camera.






