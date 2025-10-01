# NFSC Extra Options for Wine
Extra Options is a script mod which improves your gaming experience by many ways. It's developed by ExOpts Team. This is a patched version, developed to allow in-gameplay hotkeys to work in systems that use Wine compatibility layer, such as Linux.

Personally, I use it in my ROSA Linux Fresh 13 installation through Bottles flatpak, Gaming bottle preset, runner Soda 9.0-1, DXVK 2.7.1, disabled VKD3D, disabled LatencyFleX, Discrete NVIDIA graphics, GL renderer, Fsync enabled, windows 10 compatibility version, DLL overrides dinput8 (native, builtin), msvcp71 (native, builtin), msvcr71 (native, builtin).

# Download
You can [download Extra Options](https://github.com/ObmijSelaw/NFSCExOptsForWine/releases) from Releases page. If you just want to play, this is all you need.

# Compilation
BUT if you want to compile it yourself, download this repo whole , and with the x86 Command Prompt tools from Microsoft Visual Studio (2017 version worked for me in a Windows 7 Virtual Machine in Oracle Virtualbox), run these commands:
```
cd C:\Users\User\Downloads\NFSCExOptsForWine-master\NFSCExtraOptions
```

[NOTE: If your downloaded file is somewhere else, use cd and point to the actual location of your NFSCExtraOptions folder. It should contain dllmain.cpp and other files]

```
 cl /LD /O2 /I..\includes /I. dllmain.cpp stdafx.cpp /link /OUT:NFSCExtraOptions.asi user32.lib kernel32.lib
```
 This will produce a .asi file. This is the compilled mod, copy that file to your scripts folder in the Need For Speed Carbon installation folder. The required .ini and dinput8.dll can be grabbed from the release zip.
