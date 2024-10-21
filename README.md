# Awesome Eye Tracking

A list of various eye- and head-tracking software, products, datasets, etc.

**About us:**
We are *Eyes on (Dis)Abilites* and want to provide paraplegics and ALS patients with low-cost eye-tracking solutions.
This document is the result of our research on the eye- and head-tracking stuff we found.

## Projects

### On-Screen Keyboards

https://github.com/OptiKey/OptiKey ⭐ *Personal Highlight* ⭐<br>
OptiKey is an open-source on-screen keyboard designed for eye-tracking, offering layouts from simple phrase cards to full keyboards. It supports voice output, mouse control, and various eye-trackers, with plugins like one for playing Minecraft. It’s the ideal on-screen keyboard for our needs.
- 4.3k stars, last commit 3 months ago, 65 contributors
- On-Screen Keyboard with various modes, optimized for people with disabilities
- C#
- Is there a Mac port for this?
- ✔️ Tested, extremely good and versatile, has layouts for different precision levels.

https://github.com/bbenligiray/slicetype
- 14 stars, last commit 5 years ago, 1 contributor
- On-Screen Keyboard optimized for gaze-typing using circles
- C++
- Not tested yet

https://github.com/pasha-liubetski/LINKa.look-windows
- 2 stars, last commit 1 year ago, 1 contributor
- On-Screen Keyboard with cards, in Russian
- C#, .NET Framework 4.8, WPF
- Not tested yet

### Wearable-based Eye Trackers
https://github.com/pupil-labs/pupil ⭐ *Personal Highlight* ⭐<br>
Pupil-Labs produces open-source eye-tracking software and hardware. Their software was very useful for our research, though likely too complex for end-users. It allowed us to experiment with different cameras and build our first OptiKey plugin. However, their products are costly (starting at 3k€), and their DIY headset documentation lacks detail, so we sought alternative models. Still we are very happy that we found this software.
- 1.4k stars, last commit 7 months ago, 42 contributors
- Eye-tracking for wearables. Very promising
- Python, OpenCV
- ✔️ Tested, works exceptionally well. Requires some initial, somewhat tedious configuration. More details in the <a href="#Pupil-Lab">Pupil-Lab</a> section.

https://github.com/EyeTrackVR/EyeTrackVR ⭐ *Personal Highlight* ⭐<br>
EyeTrackVR offers open-source software and DIY guides for VR headset eye-tracking. With detailed documentation and affordable solutions using infrared technology, it meets many of our needs. We see great potential in this project as we continue exploring it.
- 767 stars, last commit 3 months ago, 8 contributors
- eye-tracking software and DIY instructions for eye-tracking headsets
- Python
- not tested yet

https://github.com/esdalmaijer/PyGaze
- 672 stars, last commit 2 weeks ago, 17 contributors
- Toolbox for eye-tracking
- Python (2 and 3), OpenCV, Pygame
- Not sure if also works for screen-based tracking
- ❌ we tried (on Linux) and gave up due to being very beginner-unfriendly. Confusing documentation. At least for us. :(

https://github.com/YutaItoh/3D-Eye-Tracker
- 296 stars, last commit 8 years ago, 1 contributor
- Eye-tracking software directly in front of the eye using infrared. Looks promising. C++. 2015
- C++, OpenCV
- Not tested yet

https://github.com/czero69/acomoeye-NN
- 23 stars, last commit 4 years ago, 1 contributor
- Implementation of one-shot direct gaze estimation NN based on NVGaze. Goal is for VR/AR.
- Python, Conda
- ~2.5° error rate with Acomo-14 dataset
- Not tested yet

https://github.com/gmierz/pupil-lib
- 10 stars, last commit 5 years ago, 1 contributor
- Library for processing data from Pupil Labs' eye tracker, in conjunction with [Lab Streaming Layer (LSL)](https://github.com/sccn/labstreaminglayer)
- Python, Matlab
- Not tested yet

### Screen-based Eye Trackers
https://github.com/brownhci/WebGazer
- 3.5k stars, last commit 3 months ago, 34 contributors
- JS-based eye tracking, online demo available at https://webgazer.cs.brown.edu/calibration.html
- HTML, CSS, JS
- ✔️ Online demo tested, works okay-ish.

https://github.com/vladmandic/human
- 2.2k stars, last commit 4 months ago, 9 contributors
- AI-powered 3D Face Detection & Rotation Tracking, Face Description, and more
- Node.js
- ❌ very resource intensive.

https://github.com/antoinelame/GazeTracking
- 1.9k stars, last commit 1 month ago, 7 contributors
- Webcam-based, real-time eye tracking
- Python with NumPy, OpenCV, Dlib
- Gives directions like "left", "up". Also gives a ratio from left (1.0) to right (0.0)
- ✔️ Tested. Very dependent on lighting conditions (more light != better). When it works, it provides okay-ish results. Could perhaps be used in combination with calibration to move a cursor around. Better than nothing.
- To build: Dlib doesn't build. Specific versions of Python, Dlib, and NumPy are required. (See [this Github comment](https://github.com/davisking/dlib/issues/2961#issuecomment-2183949855))
    1. Python 3.8.10
    2. Change `requirements.txt` as follows:
       ```
       dlib==19.22.99
       numpy==1.24.4
       opencv-python==4.10.0.82
       setuptools==70.0.0
       ```
    3. Install Dlib 19.22.99 manually:
        - Download precompiled from Github: [dlib-19.22.99-cp38-cp38-win_amd64.whl](https://github.com/sachadee/Dlib/raw/main/dlib-19.22.99-cp38-cp38-win_amd64.whl)
        - Install: `pip install dlib-19.22.99-cp38-cp38-win_amd64.whl`
    4. Then continue as per the project: `pip install -r requirements.txt`


https://github.com/trishume/eyeLike
- 920 stars, last commit 5 years ago, 3 contributors
- Webcam gaze tracker based on an image gradient-based eye center algorithm —no machine learning involved. According to their docs, this doesn't track gaze yet.
- C++, OpenCV
- Blog post: https://thume.ca/projects/2012/11/04/simple-accurate-eye-center-tracking-in-opencv/
- Paper: https://www.inb.uni-luebeck.de/fileadmin/files/PUBPDFS/TiBa11b.pdf
- Not tested yet (is it even testable?)

https://github.com/cpury/lookie-lookie
- 361 stars, last commit 4 years ago, 1 contributor
- AI-based eye tracking, works entirely in the browser without a backend, using TensorFlow.js
- JS, TensorFlow.js
- ✔️ Tested, works well under good lighting conditions. Trained models and datasets can be uploaded and downloaded. However, glasses confuse the tool.

https://github.com/hysts/pytorch_mpiigaze
- 346 stars, last commit 2 years ago, 1 contributor
- PyTorch implementation of MPIIGaze and MPIIFaceGaze
- Python, PyTorch
- Not tested yet

https://github.com/Ahmednull/L2CS-Net
- 310 stars, last commit 9 months ago, 4 contributors
- PyTorch implementation for gaze estimation and tracking.
- Python
- Not tested yet

https://github.com/iitmcvg/eye-gaze
- 229 stars, last commit 7 years ago, 2 contributors
- Gaze and pupil tracker
- C++
- Provides gaze direction based on head position and pupil detection
- Not tested yet

https://github.com/hugochan/Eye-Tracker
- 225 stars, last commit 6 years ago, 1 contributor
- AI-based gaze prediction, built on https://github.com/CSAILVision/GazeCapture (also listed here)
- Python
- Not tested yet

https://github.com/NativeSensors/EyeGestures
- 120 stars, last commit 0 months ago, 1 contributor
- Eye tracking. A more modern open-source Python project..
- Python
- Not tested yet

https://github.com/glefundes/mobile-face-gaze
- 93 stars, last commit 4 years ago, 1 contributor
- Gaze estimation using a neural network, based on the MPIIFaceGaze architecture (MPIIFaceGaze is a dataset)
- Python, Jupyter Notebook
- Not tested yet

https://github.com/avosskuehler/ogama
- 71 stars, last commit 2 years ago, 1 contributor
- Eye tracker, discontinued in 2016
- C#, C++
- Not tested yet

https://github.com/szydej
https://api.gazerecorder.com/
- 59 stars, last commit 4 years ago, 1 contributor
- Closed-source Windows software, can track eyes and has an API for data extraction, with an in-browser version and online demo available. Repos contain APIs.
- Backend: ???, Frontends: some C#, some JS
- ❌ Tested online demo, works (unfortunately) very well.

https://github.com/yas-sim/gaze-estimation-with-laser-sparking
- 40 stars, last commit 3 years ago, 1 contributor
- Neural network for gaze estimation
- Python, OpenVINO, NumPy, SciPy, OpenCV-Python
- Not tested yet

https://github.com/visualcamp/seeso-sample-android
- 34 stars, last commit 1 year ago, 6 contributors
- AI-based eye tracking SDK for Android
- Java
- Not tested yet

https://github.com/osama-afifi/Eye-Iris-Automatic-Detection
- 26 stars, last commit 9 years ago, 1 contributor
- Eye iris detection based on entropy & iris color score (likely screen-based)
- C++, OpenCV
- Not tested yet

https://github.com/R4j4n/Eye-Gaze_and_Blink-detection-using-Neural-Network
- 23 stars, last commit 4 years ago, 1 contributor
- AI-based eye tracking with gaze and blink detection
- Python, Jupyter Notebook
- Not tested yet

https://github.com/MustafaLotfi/Owleye
- 9 stars, last commit 1 month ago, 2 contributors
- Eye tracker (the one with the car and two webcams)
- Python, Jupyter Notebook
- Not tested yet

### Head-Tracker

https://github.com/opentrack/opentrack
- 3.6k stars, last commit 1 month ago, 54 contributors
- Head tracker middleware. Supports many input and output formats and comes pre-installed with some input trackers.
- C++
- ✔️ Very good software, particularly useful with UDP output.

### Datasets and Training Code

https://github.com/CSAILVision/GazeCapture
- 930 stars, last commit 3 years ago, 6 contributors
- Datasets, training code
- Python, Matlab
- Screen-based

https://github.com/hysts/pl_gaze_estimation
- 36 stars, last commit 3 years ago, 1 contributor
- Datasets, training code
- Python, PyTorch
- Screen-based

## Companies
- **Tobii**: Market leader in input devices for ALS patients: https://www.tobii.com/
- **Tobii competitor**: https://www.controlbionics.com/
- **Pupil-Labs**: Very expensive glasses with integrated eye tracking. Cost: ≥ €2500. However, open-source software. Also free software? German company: https://pupil-labs.com
- **Humanelektronik GmbH**: Early 2000s vibes: https://humanelektronik.de/produktkatalog/kommunikation/augensteuerung/23/augensteuerung-seetech-pro-key-15?c=31
- **Blickshift GmbH**: Software for screen-based eye tracking. Disorganized website: https://www.blickshift.com/
- **RealEye**: Studies with heat maps, from Poland: https://www.realeye.io/
- **Xcessity**: From Austria: https://iris.xcessity.at
- **Eyevido** from Koblenz, acquired by Tobii: https://eyevido.de/en/impressum/

## Products
- **Tobii Eye Tracker 5**, €279 new, €220 refurbished: https://gaming.tobii.com/product/refurbished-tobii-eye-tracker-5/
- **PCEye 5** by TobiiDynavox, ~€2500: https://www.rehamedia-shop.de/pceye-5.html

## Communities
- [r/EyeTracking](https://old.reddit.com/r/EyeTracking/)
- [r/ALS](https://old.reddit.com/r/ALS)
- [r/MND](https://old.reddit.com/r/mnd)
- https://aaccommunity.net
- https://www.specialeffect.org.uk/

## Games
- **Eye-gaze chess**: https://www.eyegazechess.com/
- **Eye-build-it (commercial startup nonsense)**: https://www.eye-build-it.de/en/eye-build-it-creator/
- **Minecraft**, playable with an Optikey keyboard fork: https://www.specialeffect.org.uk/how-we-can-help/eyemine

## Awesome Lists
- [MinjingLin's awesome gaze list](https://github.com/MinjingLin/awesome-gaze/tree/master) (Good, focused on research, many datasets. Forked from [here](https://github.com/WuZhuoran/awesome-gaze) because the original lacked dataset links)
- [RichardoMrMu's awesome gaze estimation list](https://github.com/RichardoMrMu/awesome-gaze-estimation-new) (Good, focused on research)
- [ResearchGeek's awesome eye tracking list](https://github.com/ResearchGeek/awesome-eye-tracking) (Bad, nearly empty)
- [Topless' awesome eye tracking list](https://github.com/topless/awesome-eye-tracking) (Bad, few entries, mostly outdated, dead links)

## Other Stuff
- **Augmentative and Alternative Communication (AAC)**: https://en.wikipedia.org/wiki/Augmentative_and_alternative_communication
- iOS18 has eye tracking: https://www.apple.com/newsroom/2024/05/apple-announces-new-accessibility-features-including-eye-tracking/, https://support.apple.com/guide/iphone/iphone-models-compatible-with-ios-18-iphe3fa5df43/ios
- Windows 10+ reportedly has on-screen functionality for eye tracking. Additional hardware is still required.

## Learning Materials/Videos
- [Great video for technical beginners](https://www.youtube.com/watch?v=-lmc2-podgQ)

## Building Instructions
1. [Eye of Horus - Open Source Eye Tracking Assistance](https://www.instructables.com/Eye-of-Horus-Open-Source-Eye-Tracking-Assistance/)
   - A DIY open-source eye-tracking assistance system.
2. [The EyeWriter](https://www.instructables.com/The-EyeWriter/)
   - A low-cost eye-tracking system designed for creative use, often associated with helping ALS patients draw using eye movement.

## Research on cheap Infrared Cameras
Currently recommended by us: [USB GC0308 Kamera Modul 50 Grad 0,3 Millionen Pixel MJPG/YUY2 Mini Webcam Für Windows/Android](https://de.aliexpress.com/item/1005003643369274.html)
- **Issue**: IR lights are too close together, but the size of the camera is ideal.

### Camera Specs:
- **Sensor**: GC0308, by [GalaxyCore](https://en.gcoreinc.com/)
- **Resolution**: ~640x480 (low resolution, suitable for IoT applications)

### Important Keywords:
- **Global Shutter**: Essential for accurate eye movement calculations, avoiding distortions.
  [Learn More](https://en.wikipedia.org/wiki/Rolling_shutter)
- **Monochrome/Infrared**: Only IR vision is needed, no color capture required.

### Relevant Companies:
- **GalaxyCore**: [Website](https://en.gcoreinc.com/), Shanghai
- **ArduCam**: [Website](https://www.arducam.com/), Hong Kong, focused on Arduino and Raspberry Pi camera modules
- **OmniVision**: [Website](https://www.ovt.com/), USA, with a branch in Munich
- **Leopard Imaging**: [Website](https://leopardimaging.com/), USA
- **Allied Vision**: [Website](https://www.alliedvision.com/), Germany
- **ON Semiconductors**: [Website](https://www.onsemi.com/), USA

### Camera Interfaces/Cables:
- **CSI (Camera Serial Interface)**: A standard for connecting camera sensors to boards.
  [YouTube Explanation](https://www.youtube.com/watch?v=8REu_h7bzHM)
- **I2C (Inter-Integrated Circuit)**: For communication between cameras and other devices.
  [YouTube Explanation](https://www.youtube.com/watch?v=IyGwvGzrqp8)
- **SPI (Serial Peripheral Interface)**: Another communication protocol for peripherals.
  [YouTube Explanation](https://www.youtube.com/watch?v=IyGwvGzrqp8)
- **USB with 4-pin JST connector**: A common and simple way to connect small cameras.

### Similar Sensors:
- **OV7670**
- **MT9V034**
- **GC0308**
- **OV5640**

### Night Vision Support:
- **GC0308** is specifically noted for night vision capabilities.

### Other Cameras and Products to Try:
1. [Infrarot-IR Kamera mit einstellbaren IR-LEDs](https://www.amazon.de/APKLVSR-Kompatibel-Kameramodul-Einstellbare-Infrarot-IR-LED-Licht/dp/B0CLGTM3Z8/)
2. [Adapter Board for Raspberry Pi Camera](https://www.amazon.de/Adafruit-Adapter-Thingy-Raspberry-5785/dp/B0CW22D9DM/)
3. [Weitwinkel USB Kamera](https://www.amazon.de/USB-Kameramodul-Weitwinkelobjektiv-Sicherheits%C3%BCberwachung-Industrieausr%C3%BCstung-Fahrschreiber/dp/B07S3WHRCP/)
4. [Makro-IR Kamera](https://www.amazon.de/USB-Kameramodul-USB2-0-Ausgang-Eingebettetes-300000-Pixel-Linse-Makro-Infrarotkameramodul/dp/B0B7874987/)
5. [Mini Camera Module GC0307](https://www.amazon.de/MicroMaker-Kameras-Kameramodule-Camera-GC0307/dp/B0DGMD1C9L/)
6. [Autofokus-USB Kamera OV5640](https://www.amazon.de/Kameramodul-OV5640-Autofokus-USB-Kameramodul-LinuxMac/dp/B08L6SYP6G/)
7. [Raspberry Pi IR Camera Module](https://www.amazon.de/Akozon-Infrarot-LED-Licht-Illuminator-Raspberry-Nachtsicht-Kamera-Modul-default/dp/B07GND2GWL/)
8. [Harvatek IR Emitter for Night Vision](https://www.conrad.de/de/p/harvatek-ht-170irpj-ir-emitter-850-nm-140-0805-smd-181697.html)

1. [ESP32 Development Board](https://www.amazon.de/APKLVSR-Entwicklungsplatine-Entwicklung-Dual-Core-Entwicklungsplatine-kompatibel/dp/B0CHYCFFWK/)
2. [GC0308 Camera Module](https://www.amazon.de/s?k=GC0308)

## Random Info

- **Flat connectors** and **ESP32** are important; there’s existing firmware that supports face detection.
- Example: [OV2640 Camera Module for ESP32](https://www.amazon.de/APKLVSR-OV2640-Weitwinkelobjektiv-Kameramodul-Unterst%C3%BCtzt/dp/B0D3DFJL3D/)
- The lower part contains the FTDI chip or CH340G, acting as the programmer.
- [2MP CMOS Mini Camera](https://www.alibaba.com/product-detail/2MP-CMOS-mini-camera-OV2640-Macro_1600169114277.html)
- [ESP32 with OpenCV and Robotics](https://randomnerdtutorials.com/esp32-cam-robotics-opencv-autonomous/)
- [ESP32 Camera GitHub Repo](https://github.com/espressif/esp32-camera)
- Flat Flexible Cables (FFC) and Flat Printed Cables (FPC) are crucial for these setups: [eBay Listing](https://www.ebay.de/itm/185996798993?srsltid=AfmBOoqUSf9JRRmte3ruND-2X3MxBZHbVKXdKWHfPfrcCuPRUns8XkpV)
- **OV5640**: 3W is too much for a small portable setup.
- **Valve Index Eye Tracking**: [Hackaday DIY Eye and Face Tracking for Valve Index VR Headset](https://hackaday.com/2024/05/19/diy-eye-and-face-tracking-for-the-valve-index-vr-headset/)
