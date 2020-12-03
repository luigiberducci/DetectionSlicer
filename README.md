# Detection Slicer
This repo contains the code to reproduce the SiPM Arrays acquisitions for the experiment LGND200.
It starts from G4 simulation of physical process in liquid argon and produce two kind of files:
1. detections of photoelectrons in SiPM sensor arrays
1. snapshot of acquisition over a time window

The result of this processing is then used for later analysis.

# Requirements
To run this software, you need to install `ROOT` on your pc.
The code has been tested with `ROOT 6.2.0` on `Ubuntu 18.04.5 LTS`.

# How to run
You can use the `DetectionSlicer` by compiling it:

```
$>g++ DetectionSlicer.cpp -o DetectionSlicer.exe `root-config --cflags --glibs`
$>./DetectionSlicer.exe
```

or interactively:

```
$>root
root [0] .L DetectionSlicer.cpp
root [1] DetectionSlicer("Muons", "output", "Output")
```