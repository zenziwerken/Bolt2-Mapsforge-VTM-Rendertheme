## Colors
The Wahoo Bolt2 and the Roam2 show 64 color (4<sup>3</sup>) on the display. When using Hex color only following values are used:
| Hex Value  | 
| ------------- |
| 00  |
| 55  |
| AA  |
| FF  |

On Cruiser this results in pretty screaming color, but on the reflective display they are quite nice.

Be aware that the lightest gray is `#AAAAAA`.
Make sure to create a suitable contrast!

[html presentation of avalable color](https://htmlpreview.github.io/?https://github.com/zenziwerken/Bolt2-Mapsforge-Rendertheme/blob/main/COLORS.html)

## Symbols
To adjust the size of symbols they can be scaled like this:

`<symbol src="icons/train_station.svg" symbol-percent="130"/>`

So that POI symbols do not cover too much map material in the overview, you can also use different symbols for different zoom levels.

```
<m v="supermarket">
  <m zoom-min="14">
    <symbol src="icons/supermarket_small.svg" symbol-percent="50"/>
  </m>
  <m zoom-min="15">
    <symbol src="icons/supermarket.svg"/>
  </m>
  <m zoom-min="16">
    <caption cat="bolt2" fill="#FF0000" k="name" 
     font-family="condensed" font-style="bold" priority="6" size="14" 
     stroke="#ffffff" stroke-width="3.0" dy="-16"/>
  </m>
</m>
```
![zoom14](/screenshots/zoom%2014.png)
![zoom15](/screenshots/zoom%2015.png)
![zoom16](/screenshots/zoom%2016.png)

## Railway presentation
Apart from the dashed lines there is the possibility of adding stipple strokes like this:

`<line cap="butt" fade="12" fix="true" stipple="15" stipple-stroke="#ffffff" stipple-width="0.7" stroke="#000000"  width="3" />`

## Custom tags
In the original `vtm-elemnt.xml` there are some custom tags that need to be mapped correctly. For example the tag `bic_yes` and `bic_designated`. They correspond with the [mapping-file](https://github.com/zenziwerken/Bolt2-Mapsforge-Rendertheme/blob/main/tag-wahoo.xml) at the line: `<osm-tag key='bicycle' value='bic_yes' equivalent-values='yes,public,allowed' renderable='false' />`. I added another custom tag for the surface: `bic_paved` and `bic_unpaved`.

## stylemenu
If you want to change the style according to your hardware, setting the defaultvalue does not work under the current bolt.apk. You have to swap cat-id to you desired value!

## Artefacts of natural=nosea
When rendering my first own maps I had some artefacts of `natural=nosea`. Investigating this I found that the used `land-polygons-split-4326` are – as stated – split. Problem here is the overlapping ares. So adding the tag `mesh="true"` resolves the problem. [[source]](https://github.com/mapsforge/vtm/issues/224#issuecomment-260911095)

## Screenshots
Authorize the Elemnt via adb [like so](https://github.com/treee111/wahooMapsCreator/blob/develop/docs/COPY_TO_WAHOO.md#authorize-wahoo-device). Then run
`adb exec-out screencap -p>screenshot.png`

## Screenrecord
According to the [article by DC RAINMAKER](https://www.dcrainmaker.com/2021/07/screen-record-wahoo.html) it is quite simple to create a screencapture on the Wahoo Bolt.
Create a the folder names `capture` on the bolt. Start recording by using the system menu on the bolt:

![screenshot3](/screenshots/screenshot-3.png)
