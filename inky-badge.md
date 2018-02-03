# InkypHAT Badge Holder

Next week, I'm attending the [Young Coders Conference](https://youngcodersconference.wordpress.com/) at the Tate, and I decided that I need a name bade, and what better to make one with than the wonderful [InkypHAT](https://shop.pimoroni.com/products/inky-phat) from the guys at Pimoroni.

## Creating the images

The process of getting a three-color image to correctly display on the InkypHAT is a massive faff if done wrong, and a breeze if done well.

The proper way: head over and download the [InkypHAT Repo](https://github.com/pimoroni/inky-phat). In `tools` is a nifty .gpl file that has the color palette for [Gimp](https://www.gimp.org/). On Gimp, head to Image -> Mode -> Indexed. Then open the pane located at Windows -> Dockable Dialogues -> Palettes. Click the little leftwards arrow toggle on the panel and (this took me 2 hours to find) hover over Palette Menu, and click on Import Palette.... Select the InkypHAT gpl file and you are away

The faffy way I did it: creating a 212x104 image in Illustrator, and painstakingly, pixel-by-pixel ensuring it was only three colors, (255, 255, 255), (0, 0, 0), or (255, 0, 0). This took me several hours. Then I had to invert Black and Red. This was the result:

![InkyBadge](https://raw.githubusercontent.com/3hundred4teen/3hundred4teen/master/assets/images/inky-holder/badge.png "InkyBadge")

## Creating the holder

After asking around (on the Gadgetoid server)[https://discordapp.com/invite/8wRN4WB], I found QCAD to be my best choice of CAD software. After two hours of measuring, re-measuring, and asking people for the actual sizes (and restarting the app every 15 mins on free trial), I had a design, for 3mm acrylic!

![CAD design](https://raw.githubusercontent.com/3hundred4teen/3hundred4teen/master/assets/images/inky-holder/caddesign.png "InkyBadge")

The only issue is, I had nowhere to laser cut it. (Sandy)[https://twitter.com/sandyjmacdonald] (another Pimoroni pirate) came to my rescue, and offered to have it cut out and shipped *ad gratis*. After some improvements (because I couldn't actually export the proper file type), they were cut and shipped, and they turned out beautiful!

So after hacking the `logo.py` script example, I popped the image onto the InkypHAT, screwed in the acryl plates, and this was the result!

![Badge](https://raw.githubusercontent.com/3hundred4teen/3hundred4teen/master/assets/images/inky-holder/holder-2.jpg "InkyBadge")

![Badge](https://raw.githubusercontent.com/3hundred4teen/3hundred4teen/master/assets/images/inky-holder/holder-5.jpg "InkyBadge")
