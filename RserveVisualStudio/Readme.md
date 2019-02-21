# Build Prerequisites

- Visual Studio 2017
  - Desktop development with C++
  - Windows 10 SDK (10.0.17763.0)
- Microsoft R Open 3.5.1
- zip.exe in PATH
  You can get one e.g. here: ftp://ftp.info-zip.org/pub/infozip/win32/
  
For other R versions, you need to:
- Install Microsoft R Open locally
- Update R include path in Rserve.vcxproj (2 places)
- Recreate .\Rserver\R.lib
  - Copy R.dll from c:\Program Files\Microsoft\R Open\VERSION\bin\x64 to .\Rserve.
  - Rebuild Rserve\R.lib by running generate_r_lib.bat
    Here notepad opens a file from which you must remove all entries containing "printf" except those starting with "R".
