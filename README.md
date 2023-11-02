# VSCode configuration files for working with nrf5 SDK Segger Embedded Studio projects

## Features
- Build project using `emBuild`
- Flash project using `nrfjprog`
- Debug project using `J-Link GDB Server` and `cortex-debug` 

## Requirements
- [Segger Embedded Studio](https://www.segger.com/products/development-tools/embedded-studio/)
    - bin path also needs to be added to PATH environment variable
- [nrfjprog](https://www.nordicsemi.com/Software-and-tools/Development-Tools/nRF-Command-Line-Tools/Download#infotabs)
- [J-Link Software and Documentation pack](https://www.segger.com/downloads/jlink/#J-LinkSoftwareAndDocumentationPack)
    - may already be installed with Segger Embedded Studio
- [cortex-debug](https://marketplace.visualstudio.com/items?itemName=marus25.cortex-debug)

## Usage
1. Open the project folder (where `main.c` is located) in VSCode
2. Copy the `.vscode` folder to the project folder
3. Edit the `.vscode/settings.json` file with settings below
4. In case you don't use a nRF52DK, you should change the important values in `launch.json` (e.g `device`, `svdFile`) and `c_cpp_properties.json` (e.g `defines`)

Build and Flash with `Ctrl+Shift+B`

Debug with `F5`

See tasks for more implemented options (clean, recover)

| **Setting** | **Description** |
| --- | --- |
| `debug-config` | The name of the debug configuration to use (e.g Release or Debug) |
| `softdevice` | Softdevice to use (e.g s132 or blank for no softdevice) |
| `ses-path` | Path to Segger Embedded Studio (e.g `C:/Program Files/SEGGER/SEGGER Embedded Studio for ARM 5.62`) |
| `jlink-path` | Path to J-Link Software and Documentation pack (e.g `C:/Program Files/SEGGER/JLink`) |
| `nrf-sdk-path` | Path to the nrf5 SDK (e.g `C:/nRF5_SDK_15.3.0_59ac345`) |
| `compiler-path` | Path to an ARM GCC compiler (for intellisense) |
