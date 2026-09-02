```
git clone --recursive https://github.com/EloiStree/GOMI.git
cd GOMI
git submodule foreach "git switch main"
``` 
Last Stable Build: https://eloistree.itch.io/gomi     
Last Developer Build: https://github.com/EloiStree/GOMI/releases     

Note: GOMI is an app but also a 2D Canvas in Godot if you are in XR and want to use it:  
Contact me if you want to test that for now.   


**Documentation:**   
- Video: https://www.youtube.com/@GOMI_DOC
- Text: https://github.com/EloiStree/GOMI_DOC

   
# GOMI

<img width="963" height="583" alt="image" src="https://github.com/user-attachments/assets/6485022d-6a17-4f1e-be78-ac0eab9c5071" />

**Godot Open Macro Input (GOMI)** is a system that converts input from any supported device into Godot-compatible Integer IIDs and Byte/Text packages.

**Related concepts:** OMI, XOMI, S2W, IID, and TBIO.

I previously developed a similar application in Unity.  
GOMI is a Godot-native GDScript evolution of that idea.   

## Goal (Version 1)

The initial goal is to create an application that transforms any device capable of running Godot into a universal input manager.

The primary target platforms are:

* Raspberry Pi 5
* Steam Deck + Steam Controller

Generated input packages should also be compatible with devices such as the Meta Quest 3 and Steam Frame*.

## Platform Integration

Any functionality that requires native platform APIs or external DLLs should be implemented through open-source Python scripts for the community to be sure of not be hacked.     
These scripts will handle platform-specific communication and inject the resulting values into GOMI, keeping the core project portable and transparent.   
