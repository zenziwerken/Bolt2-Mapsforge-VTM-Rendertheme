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
