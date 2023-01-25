# Parts list

Prices are correct as of January 2023.

## 1. Common optomechanical parts
Regardless of how you assemble the components, you will require the following.
| Item | Description | Approx Cost |
| --- | --- | --- |
| [MF252-39](https://www.thorlabs.com/thorproduct.cfm?partnumber=MF525-39)| Green emission filter | 220 GBP |
| [MD498](https://www.thorlabs.com/thorproduct.cfm?partnumber=MD498) | GFP dichoic | 200 GBP |
| [AC254-100-A](https://www.thorlabs.com/thorproduct.cfm?partnumber=AC254-100-A) | f=100 mm achromatic lens | 65 GBP |
| [AC254-050-A](https://www.thorlabs.com/thorproduct.cfm?partnumber=AC254-050-A) | f=50 mm achromatic lens | 65 GBP |
| [SM1A9](https://www.thorlabs.com/thorproduct.cfm?partnumber=SM1A9) | C-Mount to SM1 adapter | 16 GBP |

## 2. Optomechanical parts specific to our machined enclosure
If you are using our custom enclosure, you will need the following components.
| Item | Description | Approx Cost |
| --- | --- | --- |
| [ER05-P4](https://www.thorlabs.com/thorproduct.cfm?partnumber=ER05-P4) | 4x 1/2" cage rods | 16 GBP |
| [PFR10-P01](https://www.thorlabs.com/thorproduct.cfm?partnumber=PFR10-P01) | 25 x 36 mm camera fold mirror | 75 GBP |
| [SS6MS6](https://www.thorlabs.com/thorproduct.cfm?partnumber=SS6MS6) | 6 mm M6 set screws* to plug adjustment holes | 5 GBP |
| [SM1L10](https://www.thorlabs.com/thorproduct.cfm?partnumber=SM1L10) | 1" SM1 lens tube to house objective lens | 12 GBP |
| [SM1L05](https://www.thorlabs.com/thorproduct.cfm?partnumber=SM1L05) | 0.5" SM1 lens tube to house tube lens | 11 GBP |

*Only four set screws are needed and the pack has 25. So if you are building multiple systems, one pack is likely enough.


## 3. Fibre-coupling parts
If you wish to launch a non-fibre-coupled laser into the scan-head via a fibre then you will need to buy these parts.
If your laser is already fibre-coupled you will need only the collimating lens.
Do not buy the FibrePort and the Fibre if you have a laser that is shipped fibre-coupled.
You may also launch the laser directly into the scan-head using mirrors.
There is no parts list for this option, but if you choose it and are using the custom enclosure you will want to add a glass window over the galvo entry port. A [WG11010-A](https://www.thorlabs.com/thorproduct.cfm?partnumber=WG11010-A) is suitable.

| Item | Description | Approx Cost |
| --- | --- | --- |
| |2m fibre patch cable | 200 GBP |
| |FiberPort Collimator to launch beam into fibre | 500 GBP |
| | Collimating lens to produce a collimate beam at the scan head | 200 GBP |


## 4. The expensive parts
All systems will require the following.

### USB Camera
We have been using the [Basler ace acA1920-40um Monochrome USB 3.0 Camera](https://www.edmundoptics.co.uk/p/basler-ace-aca1920-40um-monochrome-usb-30-camera/3421/) which retails at about 550 GBP.
This camera works well.
The sensor is about 11 by 7 mm and our hardware magnifies by a factor of 0.5 so the whole sample is visible.
In principle cameras by other manufacturers will also work, but this is not currently supported by the software.
It is easier to buy the Basler camera.


### DAQ
The software requires an NI DAQ with four analog output channels.
The existing stimulators are currently using an NI USB-6363, which is acceptable in terms of performance and easy to work with.

This device comes in different formats:
* Model 782259-01 requires two BNC-2090A breakout boxes and associated cables. 3100 GBP
* Model 781443-01 is screw terminal based and so won't require breakout boxes. 3250 GBP
* Model 782258-01 has an integrated breakout box, which is easier to work with than screw terminals, but more expensive. 3800 GBP.
* Model  782257-01 is an OEM board that can potentially be integrated into a custom enclosure along with the scanner control board and associated PSUs.

Finally, there is the *possibility* that a PCIe-based device might perform a little better during the stimulus ramp down.
If you have a spare PCIe slot and do not care about the possibility of making an intergrated enclosure for all the electronics, you can buy a PCIe-6363 (781051-01, 2300 GBP) plus two BNC-2090A breakout boxes and associated cables.


### Laser
So far we have worked exclusively with the [473 nm Obis laser 75 mW](https://coherentinc.force.com/Coherent/1185052?cclcl=en_US).
These units are are quite expensive at 6000 GBP.
We have bought the free space version and fibre-coupled ourselves but a fibre-coupled version of the
Obis is also available.
The output of 75 mW is more than enough.
We are using the Obis lasers because they have proven to be reliable, stable, and switch very quickly.

Other (untested) options that are slightly different wavelength but much cheaper and in principle should work well include:
* [Oxxius 450 nm 70 mW](https://www.oxxius.com/products/lbx-405-5/) at about 2800 GBP.
* [Oxxius 488 nm 40 mW](https://www.oxxius.com/products/lbx-488/) at about 2800 GBP.
* [MatchBox 450nm 60 mW](https://integratedoptics.com/cw-lasers/450-nm-lasers/450-nm-laser-diode;-free-space) at about 1600 GBP.
* [MatchBox 488nm 40 mW](https://integratedoptics.com/cw-lasers/488-nm-lasers/488-nm-laser-diode;-free-space) at about 1600 GBP.


### Scanners
The [5 mm Saturn Scanners](https://www.edmundoptics.co.uk/p/5mm-aperture-protected-silver-saturn-5b-dual-axis-galvanometer-scanner/44527/) are generally kept in stock by Edmund and retail for 2900 GBP.
They perform very well are near silent under the conditions that we run them.
Avoid Cambridge Technologies: their lead times are around 1 year and you will need to buy a spare set to insure yourself against potential down time should the scanners fail.
Failures happen.

The scanners come with a controller card but you will also need to buy two PSUs (to generate the +/- 24 V needed).
We are using [Mean Well Switching Power Supply, 24V dc, 4.2A](https://uk.rs-online.com/web/p/switching-power-supplies/8157450), which retail at about 65 GBP each.

Please note these power supplies have exposed screw terminals carrying mains voltage.
Talk to an experienced engineer if you are unsure about wiring and housing them safely.
