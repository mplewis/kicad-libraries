# mplewis' KiCad Libraries

I use these libraries in my personal projects. Use at your own risk.

# Footprints

## Useful Stuff

### Products

[LightBlue Bean+](https://punchthrough.com/bean)

[NodeMCU Amica](http://nodemcu.com/index_en.html#fr_54747661d775ef1a3600009e)

### Manufacturer Parts

[CUI Inc. PJ-037A barrel jack](http://www.digikey.com/product-detail/en/PJ-037A/CP-037A-ND/1644545), vias and slots

[Recom Power R-78E5.0-0.5 5V fixed buck converter](http://www.digikey.com/product-detail/en/R-78E5.0-0.5/945-1648-5-ND/2834904)

[C&K Components JS202011CQN slide switch](http://www.digikey.com/product-detail/en/JS202011CQN/401-2001-ND/1640097)

[TE Connectivity FSM4JSMA 6mm tactile switch](http://www.digikey.com/product-detail/en/FSM4JSMA/450-1129-ND/525821)

[Amphenol Commercial Products 12401548E4#2A USB-C receptacle, TH/SMT, RA](http://www.digikey.com/product-detail/en/12401548E4%232A/12401548E4%232ACT-ND/5318160)

### Generic

4-pad solder jumper

SIP-3, numbered: for use with LM7805 in TO-220 form factor

Header Bus: all pins connected together

* 2x4
* 2x6
* 2x7
* 2x8

Header Strip: signals are independent with multiple pins bussed together

* 15x4 (15 individual signals, 4 pins each)

## Artwork

* [Goat](http://imgur.com/SQCLV0f) (copper, mask)
* [Nyan Pusheen](http://imgur.com/v2rxmgp) tri-color! (silk, copper, mask)

# Design Guidelines

*Reminders to myself when designing PCBs with KiCad*

Vias should be at least 0.9 mm in diameter if you expect to fit a header pin into them. Vias with diameter 0.762 mm printed at Dirty PCBs could take a header if you really forced it—make them bigger.

KiCad projects default to adding clearance to the solder mask. This makes your pads look shitty. Change this inside pcbnew: **Dimensions** –> **Pads Mask Clearance** –> **Solder Paste Clearance:** change from -0.003 to 0.

Don't squish fonts. Set the width and height equal to each other.

Font thicknesses are based on the font size. If your height/width are 0.04", the thickest KiCad will allow is 0.01" (25%). Here are some guidelines for font thickness:

* 10%: Thin
* 15%: Normal
* 20%: Bold
* 25%: Black

Extend the sides of your fill polygons a few clicks past the edge cuts. Otherwise your fill stops early at the sides and leaves pointy fill corners in your rounded corners. It looks weird.

On rounded corners:

* 0.05" radius still feels pretty pointy.
* Bean+ uses a corner radius of 10mm.

Routing works differently in OpenGL canvas mode than Default. I think?

Dirty PCBs is pretty dirty. Their silk aligning is all over the place. Don't use them for awesome custom art.

Pad size: 0.0125" annular ring pads are fine (0.025" difference between inner and outer diameter). 0.0155" pads are nice and fat and friendly.
