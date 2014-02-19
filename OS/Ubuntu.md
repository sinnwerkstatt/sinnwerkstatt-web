# Ubuntu

## Create launcher icon
* ```sudo gnome-desktop-item-edit /usr/share/applications/ --create-new```
* http://www.howopensource.com/2012/10/create-application-launcher-add-icon-to-unity-ubuntu-12-10/

## Screen recording

### ffmpeg

```
ffmpeg -f x11grab -r 25 -s 1920x1200 -i :0.0 -sameq Desktop/out.mp4
```

* press ```q``` or ```Ctrl+C``` to stop.
* other resolutions: 1280x800
* [record audio](https://trac.ffmpeg.org/wiki/How%20to%20grab%20the%20desktop%20%28screen%29%20with%20FFmpeg)

### GIF recording

* [LICEcap](http://www.cockos.com/licecap/) - only Windows and OSX.

## Webcam recording

* [guvcview](http://guvcview.sourceforge.net/) - working better than Cheese.
* [Multimedia applications](https://help.ubuntu.com/community/MultimediaApplications)

## File Synchronization

* [Unison Wiki](http://wiki.ubuntuusers.de/unison), [Unison](http://www.cis.upenn.edu/~bcpierce/unison/)

## Tips

* Disable Unnecessary Error Messages: ``gksu gedit /etc/default/apport``, set to ``enabled=0`` and ``sudo restart apport``.
