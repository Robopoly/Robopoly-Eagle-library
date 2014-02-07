# Robopoly _Eagle CAD_ library and _SketchUp_ files

![Logos](logos_robopoly_eagle.png)

## Library

The `robopoly.lbr` contains all the non-standard electrical components used in the [kit PRisme](http://robopoly.epfl.ch/prisme) for [Eagle CAD](http://www.cadsoftusa.com/download-eagle/?language=en) PCB making software. Components used for the [PRismino](https://github.com/Robopoly/PRismino), [Robopoly Shield](https://github.com/Robopoly/Robopoly-Shield) and the [Power Board](https://github.com/Robopoly/Power-Board) are all included.

## SketchUp

With [Eagle CAD](http://www.cadsoftusa.com/download-eagle/?language=en) it's possible to export PCB file to view it in 3D in [Google SketchUp](http://www.sketchup.com), a free 3D modelling software. To do so a plug-in script must be downloaded for Eagle to export the file and SketchUp to build the 3D mesh from [eagleUp website](http://eagleup.wordpress.com/). The SketchUp part file names must correspond with the component package name for them to be loaded automatically.

Follow the [tutorial on eagleUp's website](http://eagleup.wordpress.com/tutorial-v4/) to install the plug-ins and 3D files.

## Design Rule Check (DRC)

To help detecting errors and potential manufacturing problems Eagle CAD allows to run customised design rule checks that verify the PCB traces. It is by no means robust or a fail proof system, but it allows for fast checking with complex boards.

The included DRC is for Seeedstudio fusion service, it's provided by them, but one modification was needed to allow smaller distance between the PCB border and vias (needed for the Arduino pinout).

## CAM job

In order to generate files for PCBs so they could be ordered from such services as [Seeedstudio fusion service](http://www.seeedstudio.com/service/index.php?r=site/pcbService) Gerber files need to be generated. This is done by a CAM job, Seeedstudio provides this file, but some modifications were needed as the silkscreen only needs the _place_ layer and not the _names_ on the silkscreen which is selected by default.

These 8 files need to be in a .zip archive when ordering:

| File           | Description        |
| -------------- | ------------------ |
| [filename].GBL | Bottom layer       |
| [filename].GBO | Silk bottom        |
| [filename].GBS | Solder mask bottom |
| [filename].GML | Slot drills/holes  |
| [filename].GTL | Top layer          |
| [filename].GTO | Silk top           |
| [filename].GTS | Solder mask top    |
| [filename].TXT | Drills and holes   |

## Licence

The Robopoly library is published under [Creative Commons Attribution license](http://creativecommons.org/licenses/by/3.0/).

[![Creative Commons License](http://i.creativecommons.org/l/by/3.0/88x31.png)](http://creativecommons.org/licenses/by/3.0/)
