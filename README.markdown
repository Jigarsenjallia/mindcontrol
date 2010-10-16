Welcome to MindControl
======================

Introduction
------------

[MindControl][1] is a software tool that allows a researcher to utilize [optogenetics][2] to manipulate neural activity in a freely moving worm for behavioral neuroscience experiments. MindControl analyzes a video stream of a swimming nematode and in real time it generates an illumination pattern that targets specific neurons or cells within the worm. The software can output these patterns to a digital micrommirror device in a closed loop. In this way, a researcher can train arbitrary pulses of laser light only on specific cells or neurons of a worm as it moves. The software records detailed information about the worm's position, orientation and the state of the system for every frame of the video stream. This data is recorded in a human- and computer- readable YAML file. The software optionally also outputs raw and annotated video streams for later analysis. The [MindControl-analysis][3] software suite generates quantitative graphs and figures of nematode behavior based on the output from MindControl.

MindControl is the software component of [CoLBeRT] [4] (**Co**ntrolling **L**ocomotion and **Be**havior in **R**eal-**T**ime) as described in Leifer, A.M., Fang-Yen, C., Gershow, M., Alkema, M., Samuel, A.D.T., "Optogenetic manipulation of neural activity with high spatial resolution in freely moving Caenorhabditis elegans," Nature Methods, Submitted (2010).

  [1]: http://github.com/samuellab/mindcontrol
  [2]: 	http://en.wikipedia.org/wiki/Optogenetics
  [3]: http://github.com/samuellab/mindcontrol-analysis
  [4]: http://colbert.physics.harvard.edu
  [5]: http://worms.physics.harvard.edu


Authors
-------

MindControl is written by Andrew Leifer with help from Marc Gershow. It is a product of the [Samuel Lab][5] in the [Department of Physics][6] and the [Center for Brain Science][7] at [Harvard University][8]. 

  [6]: http://physics.harvard.edu/
  [7]: http://cbs.fas.harvard.edu/
  [8]: http://harvard.edu

Most Up To Date Version
-----------------------
The most up to date version of the MindControl software will always be available at http://github.com/samuellab/mindcontrol 

License
-------
With the exception of certain libraries in the `3rdPartyLibs/` folder, all of MindControl is released under the GNU Public License. This means you are free to copy, modify and redistribute this software. 


How to Cite
-----------

If you use any portion of this code or software in your research, please site:

> Leifer, A.M., Fang-Yen, C., Gershow, M., Alkema, M., Samuel, A.D.T., "Optogenetic manipulation of neural activity with high spatial resolution in freely moving Caenorhabditis elegans," Nature Methods, Submitted (2010).

Requirements
============
The software has different requirements depending on whether you plan to compile the code, or run an existing pre-compiled binary. Moreover, there are different compile targets and executables for different hardware environments. 

Pre-Built Binaries	
------------------
The quickest way to get a feel for the software is to run the VritualMC.exe pre-built executable which is packaged in an installer in the the download sections at http://github.com/samuellab/MindControl The VirtualMC.exe executable simulates camera input and micromirror output. VirtualMC.exe will run on any Windows XP system and requires only the OpenCV 1.1 run-time libraries  which are included with the provided installer. 

Compiling Your Own Binaries
---------------------------
To utilize camera or micromirror hardware functionality, you will need to compile the software from source. 

The code compiles under Windows XP. At a minimum it requires:

*	`mingw`
*	OpenCV 1.1
*	`msysgit`
*	`make`
*	`awk`

To compile any of the calibration routines additionally requires:

*	`MATLAB`

To compile an executable that uses a camera and DLP requires

*	BitFlow framegrabber SDK
*	VIALUX ALP Basic DLP USB SDK

See the `makefile` for more details about the different compile targets. 
