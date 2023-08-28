Bolt2-Mapsforge-VTM-Rendertheme
=============
This vtm-Rendertheme is based on the original from Wahoo. It will work on the
Wahoo **Bolt2** and **Roam2** (heavily tested) and the original Roam (not tested
in lack of the device). It is not intended to be used with the the original Bolt
1 and ELEMNT.

Press response
-------------
I published an article in the German [c't
Magazin](https://www.heise.de/select/ct/2022/26/2230710050673252243). It
discribes the process of creating maps and some basics for adjusting the
rendering theme.

Usage
-------------
* connect MTP via usb
* create the directory `maps\vtm-elemnt`
* copy files via Explorer to the Bolt

![screenshot](/screenshots/D72_9314.jpg)

Changes to Original:
-------------
* width and color of Cycle Trails / Paved Cycleways (initial idea of BadmanBarista)
* paved tracks -> black solid lines
* Non-paved tracks -> dashed lines
* added landuse forrest, more detailed with[^note]
* color of waterways
* highway outlines for smaller roads and bike lanes / small briges
* changed color of contruction to red dashed line
* added railways
* added labels for motorway, primary
* added labels for river
* added some pois like fuel, backery, cafe, railway station, bicycle shop[^note]
* added landuse buildings[^note]

[^note]: requires [advanced map
    material](https://github.com/treee111/wahooMapsCreator), [this
    tag-mapping-file](https://github.com/zenziwerken/Bolt2-Mapsforge-Rendertheme/blob/main/tag-wahoo.xml)
    and the attached icons

Based on the work of
[BadmanBarista](https://gist.github.com/BadmanBarista/47c34b5e9dca3910bba89c4bcdeb58b6)
