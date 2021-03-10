# Caraya-CLI-extension
Extension for G-CLI Support of Caraya

## Caraya CLI Extension

This package adds a wrapper method to the Caraya library, and allows calling Caraya from the command line using G-CLI.

Note that the native LabVIEW CLI method could be used in LabVIEW 2018 and up, however, to support CI servers which run with earlier versions of Caraya, a common library is being used (G-CLI).

## Dependencies
Caraya >= 1.1.0.x  https://github.com/JKISoftware/Caraya
G-CLI >= 2.3..x https://github.com/JamesMc86/G-CLI

## How to use

Point to "CarayaCLIExtensionEngine.vi" which installs in the Caraya root folder under <vi.lib\addons\Caraya>.
Follow the syntax as described in the Caraya wiki, but replacing the LabVIEW path with the G-CLI call, as shown in the example below:

> g-cli --lv-ver <LABVIEW_VERSION> "<LABVIEW_DIR>\vi.lib\addons\\_JKI Toolkits\Caraya\CarayaCLIExecutionEngine.vi" -- -s "<SOURCE_TEST_FOLDER>" -x "<OUTPUT_FILEPATH>"

Optional modifiers: https://github.com/JKISoftware/Caraya/wiki/Command-Line-Interface

ex:
![image](https://user-images.githubusercontent.com/11728548/110548654-e52e5700-80fe-11eb-8414-d799c999fb06.png)


## Paths supported

Caraya's "Run Tests" method supports pointing to a single file, a folder, a lvlib, a lvclass or a lvproj.
Depending on the path type selected, a single test or all tests within the container will be run. (ex: all tests in a class, all tests in a folder, all tests in a project, etc.)
