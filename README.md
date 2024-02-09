# GRAM PRI$M

# Introduction 
The **PRI$M** is a modular take on the Prism, originally designed by WunWae. It has the standard pinout for firmwares like HayBox and Pico-Rectangle, and is also compatible with more fleshed-out FGC firmwares like GP2040-CE. The key distinctive features between the original Prism and the PRI$M is the USB-C connectivity, and the modular panels that can be replaced and swapped to change the hand layouts without purchasing a whole new controller. With industrial design from GRAM, PCB designed by Quark.Works, this guide goes over a DIY-friendly approach to building and modifying the PRI$M to suit your needs.

**If you would like to support the developers of this project, consider purchasing parts like buttons, PCBs, USB-C to GCC cables, and official GRAM builds at [GRAMCTRL.COM](https://www.gramctrl.com) rather than a fab house.**

![IMG_8768 (1)](https://github.com/GrammyMoney/GRAM-x-PRISM/assets/126632196/b02a1fcf-058c-45d0-9162-b23c6b7bc4d1)

Included Files
-
Included in this repo is all the files needed to get started with a PRI$M build:
- **PRI$M Frame .stl files**
- **Aluminum Panel** Gerber files *(5 of 'em!)*
- **PCB Gerbers** for multiple hand layouts and a panelized version for the standard layout

Additional Information
-
If you want more info around GRAM builds, both open source and official builds, please join the [GRAM Digital Controllers Discord](https://discord.gg/6TuHw2r2X4) to ask questions and work with the community! I would love to see people creating new interesting designs, and building upon our initial framework.

Thanks & Acknowledgements
-
There are several people who made this project possible, either directly or indirectly.
- [Quark](https://twitter.com/quark_works), who did the PCB design on this and many other GRAM projects.
- [WunWae](https://twitter.com/WuhnWae), who developed the ergonomics and original Prism design. Thank you for your blessing on this crazy project!
- My life and business partner [BRUISES](https://twitter.com/bruisesxo), who has turned GRAM into what it is today, and had incredible patience with me as I toiled away at my computer late into the night designing this thing.

# Ordering & Customization Guide
While most of these files are universal and can be used at any fab house, **JLCPCB** has become the de-facto standard for DIY box manufacturing. This is due to their hyper-affordable pricing and low minimum order quantity.

Bill of Materials
-
Per GRAM PRI$M, you will need (some files can be made using this repository, but I will link to places to purchase them if you would like to avoid MOQs)
- 1 x PRI$M PCB set *(either panelized, or individual PCBs)*
- 1 x set of PRI$M Aluminum Panels
- 20 x [Kailh Choc V1 switches](https://www.moergo.com/products/kailh-choc-v1-key-switches-red-brown-white-pro-red-20-pack?variant=45328736780561) (Red, Red Pro, and Whites are all great choices)
- 20 x [PG1350 Hotswap Sockets](https://mkultra.click/kailh-hotswap-sockets)
- 20 x Choc v1 keycaps *(I recommend MBK profile)*
- 1 x GRAM PRI$M Frame
- 7 x [M5x0.8 8mm Low-Profile Socket Head Screws](https://www.mcmaster.com/92855A507)
- 1 x [4" JST 6-pin Socket to Socket cable assembly](https://www.digikey.com/en/products/detail/jst-sales-america-inc/A06SR06SR30K102B/9922194)
- 1 x [4" 14-pin FPC Cable](https://www.digikey.com/en/products/detail/molex/0152670295/4427171)

*Optional*
- USB-C to GCC cable for console/adapter play

Tools Needed
-
This guide assumes a level of knowledge on soldering and computer literacy. General tool requirements are:
- Soldering iron
- Solder
- USB-C to USB-A cable
- 3mm hex key/allen wrench
- Pliers
- Patience :)

The PCB
-
***Note: Since the ordering process of the PRI$M is almost identical to the [SLIM](https://github.com/GrammyMoney/GRAM-SLIM), I have used the ordering guide from the SLIM here. You may need to do more repetitions of these steps depending on which PCB you are printing, and you need to do the panel steps for all 5 aluminum panels.***

The PCB Fabrication files should come in the form of a *Gerber ZIP file* and *bom/cpl files* (usually in Excel spreadsheet formats).

Drag them into the "Upload Gerbers" box at JLCPCB and this page will pop up:

![image](https://github.com/GrammyMoney/GRAM-SLIM/assets/126632196/399c1986-c4fd-446e-97d9-e55e6c1433eb)

Here you can change the color of the PCB. Green is the fastest and cheapest from JLC, but their black PCBs look *siiiiiick*. The only setting I recommend you change is to check "**Yes**" on *Confirm Production file*. This allows for any mistakes to be ironed out by their engineers.

Towards the bottom of the page, you want to turn on the switch for **PCB ASSEMBLY**.

![image](https://github.com/GrammyMoney/GRAM-SLIM/assets/126632196/349919ce-35f1-425e-aabc-416f8ca25363)

Make sure you are assembling the *Bottom Side* of the PCB, and make sure to set *Confirm Parts Placement* to "**Yes**". None of the advanced options need to be changed.

Upon confirming your PCB Assembly options, you'll be taken to the Assembly wizard. Clicking next will give you a location to upload the *BOM* and *CPL* files (*CPL* is referred to as *Positions* in the GRAM Slim files). Once you click through, you'll be brought to you BOM list.

![image](https://github.com/GrammyMoney/GRAM-SLIM/assets/126632196/36b6bb49-a48a-4550-983b-55a35bed7615)

This will allow you to modify parts if there's any low stock. There's a line at the bottom for CH1-CH21 with some red text. This is for assembling hotswap sockets, which is not recommended for JLC, as you have to preorder them. when you click **next**, continue by clicking *Do not place*.

![image](https://github.com/GrammyMoney/GRAM-SLIM/assets/126632196/b6534da2-4ae0-4e29-a1a3-f0b06aea3565)

The wizard looks intimidating, but good news! Since you're confirming part placement, the JLC engineers will fix any errors. Just go ahead and continue.

There you have it! Your PCB is ready to order. As of the time of this writing, a set of 5 assembled boards costs $56.07 before shipping.

The Panels
-
The process of ordering aluminum panels from JLC is similar to the PCB ordering process, but much simpler. Start by dragging the **GRAM Slim Top** Zip file into the JLC upload window. We want an aluminum PCB, 1.6mm. You can choose either white or black coating (white tends to be glossy, black is matte but a fingerprint magnet). 

![image](https://github.com/GrammyMoney/GRAM-SLIM/assets/126632196/cfec88fb-68bb-479e-8c88-61d2a660c8fc)

Under High-spec Options, make sure to remove order number, or else they'll put an ugly serial number on the panel.

Once you save to cart, you'll see this screen:

![image](https://github.com/GrammyMoney/GRAM-SLIM/assets/126632196/218c9ba4-145b-4697-92de-b3484fcedc13)

Here you can add the **GRAM Slim Bottom** Zip file, and it will copy all your settings from the Top panel. Save to cart, and you're ready to check out with your PCBs!

*Note: JLCPCB cannot transact PCB and 3D printing orders together, so place this order, then move on to 3D printing.*


The Frame
-
The frame file is pretty self explanatory. Just go into JLC's 3D printing section, drop the STL file in, and choose your material. I recommend black Resin, but LEDO 6060 is a great, low cost alternative. The only material I recommend against is the textured Nylon options, as the tolerances between the frame and panels are extremely tight, and the texture could interfere with that. make sure the surface finish is set to *sanded*. 

The website will flag some possible errors (Inverted normals, Multi-shells, Possible noise shells) but if you have not modified the .stl file you are good to go. It is also possible that their support contact you about a risk of deformation given the geometry of the workpiece but it is normal and you should reply to the email that you accept the risks.


![image](https://github.com/GrammyMoney/GRAM-SLIM/assets/126632196/7fee3cdb-1453-4f1a-8c41-a377b9aa191a)

Need help building your PRI$M? Feel free to join our [Discord](https://discord.gg/gramctrl) for advice from our lovely open source community!
