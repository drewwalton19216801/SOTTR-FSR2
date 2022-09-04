# SOTTR-FSR2 (FidelityFx Super Resolution 2.0 for Shadow of the Tomb Raider)
Drop-in DLSS replacement with FSR 2.0 for Shadow of the Tomb Raider

## Installation
*Following instructions were written for Shadow of the Tomb Raider and may differ for other games.*
### Windows 
* No releases for now

### Linux
* No releases for now

### Uninstallation
* Just run `DisableSignatureOverride.reg`
* Linux users should refer to prior command.

## Compilation

### Requirements
* Visual Studio 2022
* latest Vulkan SDK (1.3.216.0)

### Instructions
* Clone this repo with all of its submodules.
* Compile the FSR 2.0 submodule in external/FidelityFX-FSR2 as instructed in [official documentation](https://github.com/GPUOpen-Effects/FidelityFX-FSR2#quick-start-checklist). Note: I used the GenerateSolutionsDLL.bat but I am sure static libraries will work fine too.
* Open the CyberFSR.sln with Visual Studio 2022.
* Hit Compile.
* Copy the compiled `ffx_fsr2_api_dx12_x64.dll` and `ffx_fsr2_api_x64.dll` from the FidelityFX Directory to your Shadow of the Tomb Raider executable directory.
* Rename the compiled DLL to `nvngx.dll`.
* Run the `EnableSignatureOverride.reg` to allow SOTTRs DLSS implementation to load unsigned DLSS versions
* Run the game and set the quality in the DLSS settings
* Play the game with FSR 2.0