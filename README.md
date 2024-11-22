# Awesome Eye Tracking

A list of various eye- and head-tracking software, products, etc.

**About us:**
We are (Eyes on (Dis)Abilites)[https://gaming.ifb-stiftung.de/eyes-on-disabilities-der-startschuss/] and we want to provide low-cost eye-tracking solutions to paraplegics and ALS patients.
This document is the result of our research. The focus is mostly on software, hardware, and products, and not on datasets and studies.

# Table of Contents
- [Projects](#projects)
   - [On-Screen Keyboards](#on-screen-keyboards)
   - [Wearable-based Eye Trackers](#wearable-based-eye-trackers)
   - [Screen-based Eye Trackers](#screen-based-eye-trackers)
   - [Head-Tracker](#head-tracker)
- [Companies](#companies)
- [Commercial Software and Devices for Individuals](#commercial-software-and-devices-for-individuals)
- [Communities](#communities)
- [Games](#games)
- [Awesome Lists](#awesome-lists)
- [Other Stuff](#other-stuff)
- [Learning Materials/Videos](#learning-materialsvideos)
- [Building Instructions](#building-instructions)
- [Research on cheap Infrared Cameras](#research-on-cheap-infrared-cameras)
   - [Camera Specs:](#camera-specs)
   - [Important Keywords:](#important-keywords)
   - [Relevant Companies:](#relevant-companies)
   - [Camera Interfaces/Cables:](#camera-interfacescables)
   - [Similar Sensors:](#similar-sensors)
   - [Night Vision Support:](#night-vision-support)
   - [Other Cameras and Products to Try:](#other-cameras-and-products-to-try)
- [Random Info](#random-info)


## Projects

### On-Screen Keyboards

https://github.com/OptiKey/OptiKey ⭐ _Personal Highlight_ ⭐<br>
_OptiKey is an open-source on-screen keyboard designed for eye-tracking, offering layouts from simple phrase cards to full keyboards. It supports voice output, mouse control, and various eye-trackers, with plugins like one for playing Minecraft. It’s the ideal on-screen keyboard for our needs._

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

https://github.com/pupil-labs/pupil ⭐ _Personal Highlight_ ⭐<br>
_Pupil-Labs produces open-source eye-tracking software and hardware. Their software was very useful for our research, though likely too complex for end-users. It allowed us to experiment with different cameras and build our first OptiKey plugin. However, their products are costly (starting at 3k€), and their DIY headset documentation lacks detail, so we sought alternative models. Still we are very happy that we found this software._

- 1.4k stars, last commit 7 months ago, 42 contributors
- Eye-tracking for wearables. Very promising
- Python, OpenCV
- ✔️ Tested, works exceptionally well. Requires some initial, somewhat tedious configuration. More details in the <a href="#Pupil-Lab">Pupil-Lab</a> section.

https://github.com/EyeTrackVR/EyeTrackVR ⭐ _Personal Highlight_ ⭐<br>
_EyeTrackVR offers open-source software and DIY guides for VR headset eye-tracking. With detailed documentation and affordable solutions using infrared technology, it meets many of our needs. We see great potential in this project as we continue exploring it._

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

https://github.com/opentrack/opentrack ⭐ _Personal Highlight_ ⭐<br>
_Opentrack is a middleware for various head-tracking inputs and outputs. Some of the inputs are already included within Opentrack and don't require any additional software. We love Opentrack for its effortless usage. With the UDP output we were able to easily test our calibration software with real tracker data without any extra hardware._ 

- 3.6k stars, last commit 1 month ago, 54 contributors
- Head tracker middleware. Supports many input and output formats and comes pre-installed with some input trackers.
- C++
- ✔️ Very good software, particularly useful with UDP output.

https://github.com/AIRLegend/aitrack

- 1.1k stars, last commit  2 years ago, 6 contributors
- A 6DOF head-tracker, which pushes the data over UDP. Very compatiple with Opentrack.
- C++
- ✔️ While a little resource hungry, still very good.
The output format of the head-tracking data is the same as the one from Opentrack.
So if you are just interested in the data over UDP, and you don't care about calibrating the data first, you actually don't need Opentrack.

## Companies

Tobii AB https://www.tobii.com/:
- produces: eye-tracking software and hardware, both for health care and for individuals.
Its subsidiary [Tobii Dynavox AB](https://www.tobiidynavox.com/) focusses on assistive technology, like tables with integrated eye-tracking software.
- location: Sweden
- revenue: [SEK 758 million in 2023](https://a.storyblok.com/f/149538/x/8cfe9a91b4/year-end-report-q4-2023.pdf).
See more at [Tobii's finance publications](https://corporate.tobii.com/investors/financial-publications).

Pupil-Labs https://pupil-labs.com/:
- produces: eye-tracking software and wearable hardware, mostly for research applications.
- location: Germany

others:
- Natural Point, Inc., known for its _TrackIR_ head tracker: https://www.naturalpoint.com/, https://www.trackir.com/
- Eye Tech Digital Systems, Inc.: https://eyetechds.com
- Tobii competitor: https://www.controlbionics.com/
- Humanelektronik GmbH: Early 2000s vibes: https://humanelektronik.de/produktkatalog/kommunikation/augensteuerung/23/augensteuerung-seetech-pro-key-15?c=31
- Blickshift GmbH: Software for screen-based eye tracking. Disorganized website: https://www.blickshift.com/
- RealEye: Studies with heat maps, from Poland: https://www.realeye.io/
- Xcessity: From Austria: https://iris.xcessity.at
- Eyevido: from Koblenz, acquired by Tobii: https://eyevido.de/en/impressum/

## Commercial Software and Devices for Individuals

A disclaimer: Our goal is to provide cheap or even free and eye-tracking solutions.
We therefore don't want to encourage you to buy the following listed solutions.
However, for transparency, we want to present these commercial products we found.
The list contains the newest version of the products. Their predecessors might still be available.

- Tobii Eye Tracker 5, 279€ new, 220€ refurbished: https://gaming.tobii.com/product/refurbished-tobii-eye-tracker-5/
- TrackIR 5, 142,47€: https://www.trackir.com/trackir5/
- BEAM Eye Tracker, 29€: https://beam.eyeware.tech/get-beam/

## Communities

- [r/EyeTracking](https://old.reddit.com/r/EyeTracking/)
- [r/ALS](https://old.reddit.com/r/ALS)
- [r/MND](https://old.reddit.com/r/mnd)
- https://aaccommunity.net
- https://www.specialeffect.org.uk/

## Gaming

- Eye-gaze chess: https://www.eyegazechess.com/
- EyeMine: An Optikey keyboard fork for playing **Minecraft** with your eyes: https://www.specialeffect.org.uk/how-we-can-help/eyemine
- OKGO: An Optikey keyboard fork for playing various games like **Portal**: https://github.com/kmcnaught/OKGO

## Awesome Lists

- [MinjingLin's awesome gaze list](https://github.com/MinjingLin/awesome-gaze/tree/master) (Good, focused on research, many datasets. Forked from [here](https://github.com/WuZhuoran/awesome-gaze) because the original lacked dataset links)
- [RichardoMrMu's awesome gaze estimation list](https://github.com/RichardoMrMu/awesome-gaze-estimation-new) (Good, focused on research)
- [ResearchGeek's awesome eye tracking list](https://github.com/ResearchGeek/awesome-eye-tracking) (Bad, nearly empty)
- [Topless' awesome eye tracking list](https://github.com/topless/awesome-eye-tracking) (Bad, few entries, mostly outdated, dead links)

## Learning Materials/Videos

- [Great video for technical beginners](https://www.youtube.com/watch?v=-lmc2-podgQ)

## DIY Hardware

- [Example 1 of a head-mounted camera](https://www.instructables.com/Eye-of-Horus-Open-Source-Eye-Tracking-Assistance/)
- [Example 2 of a head-mounted camera](https://www.instructables.com/The-EyeWriter/)
- [Hackaday DIY Eye and Face Tracking for Valve Index VR Headset](https://hackaday.com/2024/05/19/diy-eye-and-face-tracking-for-the-valve-index-vr-headset/)

## Other Stuff

- **Augmentative and Alternative Communication (AAC)**: https://en.wikipedia.org/wiki/Augmentative_and_alternative_communication
- iOS18 has eye tracking: https://www.apple.com/newsroom/2024/05/apple-announces-new-accessibility-features-including-eye-tracking/, https://support.apple.com/guide/iphone/iphone-models-compatible-with-ios-18-iphe3fa5df43/ios
- Windows 10+ reportedly has on-screen functionality for eye tracking. Additional hardware is still required.
