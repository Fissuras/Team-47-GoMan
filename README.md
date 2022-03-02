# Team-47-GoMan
Source Code for Team 47 GoMAN
Originally from http://web.archive.org/web/19990429231514/http://www.47-tek.com/source.htm

It seems these files disappeared from the net a long time ago. At Wikipedia there is a note that says "currently there are no known mirrors on the web; the source code seems as of 2017 to be lost".
Well, I've found them on an old CD backup, so here they are. 

Team 47 GoMan Source Code

47-TEK would like to thank the gaming community for its support over the years and hopes that the memory of our work can live on by releasing out the source code and shareware versions of our titles for free to the public.

The following links will allow you to download the source code for Team 47 GoMan, tools to convert 3DS rev 4 to our proprietary model & animation format, as well as the original models for the game. We are releasing this code for the purpose of helping out any software or hardware company that is working with DirectX. There are no restrictions for the use of this code. It can be incorporated into any product you wish, including products you will sell commercially. 47-TEK does not warrant or guarantee any of this material and will not support it in any way.  You cannot use any of the original art or sound resources.  The characters and storyline remain the exclusive property of 47-TEK, Inc and its shareholders.  The interactive rights based on this content remain the exclusive property of Coconuts Entertainment Japan Inc.

Here are the files
SOURCE + INCLUDE ........ 	.........TOOLS .......... 	.........ORIGINAL ART.......... 	.....MODEL TEXTURES ....
654K
updated 5.9.98
with .mak file, script1.rc, etc 	387K 	4.6 MB 	

574K

Notes: You will need to rename robota~1.h to robotani.h & rename robotm~1.h to robotmov.h, and also rename robota~1.c to robotani2.c & rename robotm~1.c to robotmov2.c. You will also need to add DirectX SDK, DDK and MSVC files to your directory path so that essential fils from these 2 SDK's can be linked in. Please visit Microsoft to get these files. The following is a list of these files :
(dplayx.lib dsound.lib dinput.lib msacm32.lib d3drm.lib ddraw.lib winmm.lib libc.lib kernel32.lib user32.lib gdi32.lib winspool.lib comdlg32.lib advapi32.lib shell32.lib ole32.lib oleaut32.lib uuid.lib odbc32.lib odbccp32.lib version.lib mmddk.h windows.h mmsystem.h)

The texture files above should go with the models in the original art. Other art can be found in the single level free download of the goman demo. The shareware version can be compiled by going into the build / settings / C++ area and adding the following to the preprocessor settings: SHARE640 or SHARE512 (D3D), or SHARE320 (software only).


The following is some information regarding this engine:

Background:

This engine began its life as a higher level gaming system built upon the Criterion Renderware(R) API, which game rise to the first true 3D fighting games for the PC, Sentoo & Creep Clash. It was then re-written from the bottom up to utilize the Reality Lab 3D API, from Rendermorphics. Once Reality Lab was licencesed to Microsoft, this API then evolved into the Microsoft D3D API, which is the 3D current cornerstone of Microsoft’s DirectX Foundation.


Engine Features:

Machine Detection Features:

In order to provide the best possible ‘out of box’ experience to the end user, we have dedicated a great deal of effort into the detection portion of our engine that will give our program key information about the end user’s machine. We will detect their available memory on their HDD, system memory, as well as Video memory. We also detect the CPU type (Pentium, MMX or Pentium Pro), input device type, as well as check for the presence of a D3D compatible VGA accelerator. If we find a D3D accelerator, we will also check deeper to determine which features it supports, then we will provide defaults and options for the end user that will give them the best quality experience possible on their hardware. Because of this feature, we are able to cupport more than 15 different 3D chips all with only one EXE file!


3D Features:

The 3D portion of our engine runs within D3D’s retained mode, in order to have access to the retained mode features. However, all of the game rendering is written in immediate mode, which is the more optimized layer of the D3D API. By using this 'mixed' D3D approach, we are able to utilize the best features of the retained mode API, without sacrificing any performance in our game render loop. 47-TEK is a leader in this area; the following quote regarding our first title created with this engine give an example of what other industry leaders have said about our game & engine.

"Team 47 GoMan(tm) is the most impressive Direct3D Retained Mode application we've seen running on Voodoo Graphics. Players can select the highest detail level with advanced alpha-blending techniques to give the no compromise game experience Voodoo Graphics owners have come to expect in 3D games." Brian Bruning, 3DFX


Physics:

Our engine also has real world physics built in to provide for a greater submodal connection between the user to the avatar or player-character in the 3D world. Physical attributes such as mass, velocity, strength & momentum can all be controlled in a precise manner for each different character.

3D Animation Features:

In order to provide for faster loading time, as well as an increased amount of animations available to the player, 47-Tek has developed its own model and quaternion-based animation file format to replace the format provided by DirectX. This file format allows us to have animation files sizes less than 1/10 the size of the Microsoft file, while still maintaining complete compatibility with DirectX. These file formats and related interpretive functions are proprietary to 47-TEK.


2D Features:

In addition to providing for 3D game experience, our engine provides high level 2D functions that allow us to create a very intuitive 'wrapper' around the 2D game. These features include bitmap display with highlighting, movie playback, as well as overlay functions for features such as score or radar displays.


5D Features:

These are features that combine 2D & 3D techniques to create an experience that give the quality of 2D without sacrificing the free interactivity of real-time 3D. We are able to create a more rich user environment by using animating 2D techniques on 3D ‘particles’ generated by our particle system engine. These 'particles' can come to life in the form or elements such as dust, plasma weapons, fire, smoke. In addition to these, 2D decals of small objects (tree’s, light posts, etc) as well as a scrolling 2D background, provides a more complete user experience that helps maintain the suspension of disbelief necessary to keep the end user completely connected to our interactive experience. If we attempted to create the same amount of 'depth' or realism with only 3D technology, the strain on the end user machine would be too great, and the framerate & gameplay would not be sufficient to make the end product viable in the marketplace.


Sound Features:

We have built our own sound functions on tope of the sound functions provided in the DirectSound API. These functions provide for MIDI & SFX playback, as well as changes in velocity according to camera positioning in order to create a 3D sound effect. We also provide for control of the music & SFX volume from within the games, so the user does not have to exit the game to make changes.


Input Features:

Our input section will allow for simultaneous use of mouse, joystick & keyboard, as well as end user configurability. We will detect if you have a 2 button or 4 button analog joystick, then provide different configuration options from with to choose. If we detect a Direct Input supported device, we will automatically load a custom configuration, as well as a bitmap in the options section that will give the complete layout for the controller. Support for Microsoft’s Gaming Device Profiler is also provided, which allows the end user to self configure and save configurations for the Microsoft Sidewinder 3D Pro(tm) & Microsoft Sidewinder Gamepad(tm).


Detail Settings:

We auto sense the end user’s machine and provide for a detail setting that is most appropriate for their machine as a default. The end user can also change the detail settings in the options menu to change the features used according to what is supported by their machine. The detail settings will effect the size of the landscape seen, as well as determine which D3D features will be used, e.g. perspective correction, color key transparency, alpha transparency, alpha blending, bilinear filtering, as well as directional lighting.


Difficulty Settings:

We provide for various levels of difficulty in our engine, in order make the end product playable to all levels of end user, from beginner to expert game player.


Load / Save Features:

This engine element allows us to save gaming states so that the end user can some back to where they left off. The 3D experiences created with this engine will definitely take time to explore and master, therefore this type of feature is essential.

EOM 
