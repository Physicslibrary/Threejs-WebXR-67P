# Threejs-WebXR-67P

Visualize the size of comet 67P/Churyumov-Gerasimenko in Oculus Quest.

<img src="images/com.oculus.vrshell-20200104-104034.jpg" width="640">

<img src="images/com.oculus.vrshell-20200104-105029.jpg" width="640">

Rosetta 1km from 67P comet.

<img src="images/com.oculus.vrshell-20200104-105252.jpg" width="640">

Rosetta 10km from 67P comet.

This project was inspired by a European Space Agency's webpage explaining the relative size of the Rosetta space probe to comet 67P/Churyumov-Gerasimenko:
 
[ESA: How big is Rosetta compared with the comet?](http://sci.esa.int/rosetta/54831-how-big-is-rosetta-compared-with-the-comet/)
 
With ESA and NASA open sourcing their data such as 3D models and images, Three.js, a modern web browser with WebXR, and Blender can be used to visualize models of a comet (4100m) and Rosetta (32m) in virtual reality.

# Threejs-WebXR-67P Pages

[https://physicslibrary.github.io/Threejs-WebXR-67P](https://physicslibrary.github.io/Threejs-WebXR-67P)

# Hardware

Oculus Quest recommended (required 6DOF headset/controllers).<br>

# Software

Oculus Browser (Oculus Quest Firmware update 12.0 or later).

# Installation

No installation. In Oculus Quest, open Oculus Browser and go to link:

[https://physicslibrary.github.io/Threejs-WebXR-67P/examples/67P-Rosetta-1-to-100-scale.html](https://physicslibrary.github.io/Threejs-WebXR-67P/examples/67P-Rosetta-1-to-100-scale.html)

[https://physicslibrary.github.io/Threejs-WebXR-67P/examples/67P-Rosetta-1-to-1-scale.html](https://physicslibrary.github.io/Threejs-WebXR-67P/examples/67P-Rosetta-1-to-1-scale.html)

With Oculus Quest's headset 6DOF tracking, freely walk around Rosetta/67P within Oculus Guardian system. Use Oculus Touch controllers to go to areas out of reach.<br>

Use Oculus Touch controllers to "fly" around Rosetta and comet 67P. It implements a simple way to move around 3D by making a "velocity vector" from left to right controllers.<br>

The distance between controllers is the speed (next to each other is the lowest speed).<br>

Press one front trigger to move (two triggers to double speed).<br>

Hold the left controller fixed and point the right controller in the direction to move.<br>

The simple "fly" code is based on webvr_vr_ballshooter.html before the recent three.js update to WebXR in December 2019.<br>

Note - The white lines from the controllers are not for pointing direction to move but with seeing where the controllers are (codes from webvr_vr_ballshooter.html). The line is approx 1m in length so it good for something like getting rough measurement of Rosetta.<br>

Other buttons on controllers do not work, yet.<br>

# Credits
 
ESA\_Gaia\_DR2\_AllSky\_Brightness\_Colour\_Cartesian\_2000x1000.png<br>
Date: 25 April 2018<br>
Satellite: Gaia<br>
Copyright: ESA/Gaia/DPAC, CC BY-SA 3.0 IGO<br>
[http://sci.esa.int/gaia/60196-gaia-s-sky-in-colour-equirectangular-projection/](http://sci.esa.int/gaia/60196-gaia-s-sky-in-colour-equirectangular-projection/)<br>
 
CSHP\_DV\_257\_01\_\_\_\_\_\_\_00343.obj (OBJ File 3.8MB)<br>
Copyright: ESA/Rosetta/NAVCAM – CC BY-SA IGO 3.0<br>
[https://imagearchives.esac.esa.int/index.php?/page/navcam_3d_models](https://imagearchives.esac.esa.int/index.php?/page/navcam_3d_models)<br>
[https://imagearchives.esac.esa.int/index.php?/page/copyright_information](https://imagearchives.esac.esa.int/index.php?/page/copyright_information)<br>

Rosetta.blend (Rosetta.zip 4MB)<br>
Author/Origin: Eyes on the Solar System. NASA/JPL-Caltech<br>
[https://nasa3d.arc.nasa.gov/detail/eoss-rosetta](https://nasa3d.arc.nasa.gov/detail/eoss-rosetta)<br>
[https://www.nasa.gov/multimedia/guidelines/index.html](https://www.nasa.gov/multimedia/guidelines/index.html)<br>

Blender 2.81 (or latest) is used to scale CSHP\_DV\_257\_01\_\_\_\_\_\_\_00343.obj to 4100m and exported as "glTF Binary" 67P.glb. 

Rosetta.blend (2012 version) is opened with Blender 2.81, fixed few broken things, and exported as "glTF Binary" rosetta.glb.
 
https://www.blender.org/

km_markers.glb is created in Blender as a series of 10x10x10m cubes spaced by 1km to give a sense of distance.

# References

[https://threejs.org/](https://threejs.org/)

[https://github.com/mrdoob/three.js/](https://github.com/mrdoob/three.js/)

Three.js examples is the best place to learn and experiment:

[https://github.com/mrdoob/three.js/tree/dev/examples](https://github.com/mrdoob/three.js/tree/dev/examples)

Three.js' excellent documentation on how to convert WebGL examples to WebVR:

[https://threejs.org/docs/index.html#manual/en/introduction/How-to-create-VR-content](https://threejs.org/docs/index.html#manual/en/introduction/How-to-create-VR-content)

Three.js example of how to use the controllers:

[https://github.com/mrdoob/three.js/blob/dev/examples/webxr_vr_ballshooter.html](https://github.com/mrdoob/three.js/blob/dev/examples/webxr_vr_ballshooter.html)

Three.js example of how to load .glb file:

[https://github.com/mrdoob/three.js/blob/dev/examples/webgl_loader_gltf.html](https://github.com/mrdoob/three.js/blob/dev/examples/webgl_loader_gltf.html)

Near the end of the webpage is an example of displaying an equirectangular map:

[https://threejsfundamentals.org/threejs/lessons/threejs-backgrounds.html](https://threejsfundamentals.org/threejs/lessons/threejs-backgrounds.html)

[https://www.blender.org/](https://www.blender.org/)

[Rosetta and comet 67P to scale](https://sci.esa.int/web/rosetta/-/54829-rosetta-and-comet-67p-to-scale-annotated)

# Making Threejs-WebXR-67P (experimental Feb 10, 2020)

This section assumes users know what a Raspberry Pi single-board computer is and how to use a Linux terminal.

Threejs-WebXR-67P is developed on a Raspberry Pi Model 3B+ by coding three.js HTML5 files and Node.js to serve them:

[https://threejs.org/docs/index.html#manual/en/introduction/How-to-run-things-locally](https://threejs.org/docs/index.html#manual/en/introduction/How-to-run-things-locally)

Raspberry Pi Model 3B+ has an ethernet port and wireless LAN. We will be making the Pi into a wifi server to connect the Oculus Quest. Learn more about Raspberry Pi at:

[https://www.raspberrypi.org/](https://www.raspberrypi.org/)

[https://www.raspberrypi.org/help/](https://www.raspberrypi.org/help/)

Get Raspbian Buster with desktop (tested February 2020, 1138 MB version) from:

[https://www.raspberrypi.org/downloads/raspbian/](https://www.raspberrypi.org/downloads/raspbian/)

Make a bootable Raspbian micro SD card:

[https://www.raspberrypi.org/documentation/installation/installing-images/README.md](https://www.raspberrypi.org/documentation/installation/installing-images/README.md)

Connect to the internet using the ethernet port. The wireless LAN will be reconfigured and not available for internet connection.

After booting Raspbian and finishing initial setup, start configuring the Pi as a wireless access point:

[https://www.raspberrypi.org/documentation/configuration/wireless/access-point.md](https://www.raspberrypi.org/documentation/configuration/wireless/access-point.md)

In the "Configuring the access point host software (hostapd)", make own NameOfNetwork and good passwork for wpa_passphrase. For this experiment, the author finishes at "Start it up" to keep thing simple (so no internet using wireless LAN but apt-get on Pi from ethernet).

Review Terminal:

[https://www.raspberrypi.org/documentation/usage/terminal/](https://www.raspberrypi.org/documentation/usage/terminal/)

In a Terminal, run:

sudo apt-get install npm

sudo apt-get install http-server -g

(Ref: [https://www.npmjs.com/package/http-server](https://www.npmjs.com/package/http-server))

In home directory,

mkdir webvr<br>

cd webvr<br>

openssl req -newkey rsa:2048 -new -nodes -x509 -days 3650 -keyout key.pem -out cert.pem<br>

The command is from the preceeding link in section "TLS/SSL".

Open Chromium, and go to:

[https://threejs.org/](https://threejs.org/)

Click "download" and three.js-master.zip should download.

After download is completed, extract three.js-master.zip to webvr.

In webvr directory, type:

http-server . -p 8000 -S

In Chromium, enter ```https://127.0.0.1:8000``` and should get a warning "Your connection is not private". Proceed in "Advanced" as you are connecting to your own Raspberry Pi.

Should see something like: (picture)

Go to three.js-master, examples: (picture)

If the above work on Raspberry Pi, wifi connect Oculus Quest to Pi, open Oculus Browser, enter ```https://192.168.4.1:8000```.

<img src="images/com.oculus.vrshell-20200209-142707.jpg" width="640">


Blender 2.81 imports 3D models CSHP\_DV_257\_01\_\_\_\_\_\_\_00343.obj and Rosetta.blend, and exports to format three.js can read.

<br>Copyright (c) 2019 Hartwell Fong
