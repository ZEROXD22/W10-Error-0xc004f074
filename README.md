### Windows 10 Activation Script Without Software

This is a simple batch script to activate various editions of Windows 10 without requiring additional software. The script provides valid product keys for editions such as Home, Professional, Education, and Enterprise.

### How to Use

1. Right-click on the `.bat` file.
2. Before running the script, temporarily disable Windows Defender or any antivirus software on your computer.
3. Choose "Run as Administrator" to ensure the script runs with full administrative rights.
4. Wait for the activation process to complete. The script will attempt to connect to the KMS activation server.
5. After activation is successful, you can re-enable Windows Defender or antivirus software.

### Notes

- Make sure your computer is connected to the internet during the activation process. If you encounter issues, ensure that the product key used matches the installed version of Windows 10.

### License

This script is licensed under the MIT License. Details can be found in the LICENSE file.

### Contribution

You are welcome to contribute to the development of this script. Please create pull requests for fixes or feature enhancements.

### Warning

This script is not an official solution from Microsoft. The use of this script is at the user's own risk. The author is not responsible for any issues or damages that may arise from using this script. Use it at your own risk.

### Testing Notes

This script has been tested using Windows 10 Pro and was successful. However, results may vary depending on the version of Windows 10 used.

---

@echo off

title Aktivasi windows 10 Gratis Tanpa Software!&cls&echo ============================================================================&echo #Project: Activating Microsoft software products for FREE without software&echo ============================================================================&echo.&echo #Supported products:&echo - windows 10 Home&echo - windows 10 Home N&echo - windows 10 Home Single Language&echo - windows 10 Home Country Specific&echo - windows 10 Professional&echo - windows 10 Professional N&echo - windows 10 Education&echo - windows 10 Education N&echo - windows 10 Enterprise&echo - windows 10 Enterprise N&echo - windows 10 Enterprise LTSB&echo - windows 10 Enterprise LTSB N&echo.&echo.&echo ============================================================================&echo Mengaktivasi windows 10 anda, silahkan tunggu...&cscript //nologo slmgr.vbs /ckms >nul&cscript //nologo slmgr.vbs /upk >nul&cscript //nologo slmgr.vbs /cpky >nul&set i=1&wmic os | findstr /I "enterprise" >nul
if %errorlevel% EQU 0 (cscript //nologo slmgr.vbs /ipk NPPR9-FWDCX-D2C8J-H872K-2YT43 >nul&cscript //nologo slmgr.vbs /ipk DPH2V-TTNVB-4X9Q3-TJR4H-KHJW4 >nul&cscript //nologo slmgr.vbs /ipk WNMTR-4C88C-JK8YV-HQ7T2-76DF9 >nul&cscript //nologo slmgr.vbs /ipk 2F77B-TNFGY-69QQF-B8YKP-D69TJ >nul&cscript //nologo slmgr.vbs /ipk DCPHK-NFMTC-H88MJ-PFHPY-QJ4BJ >nul&cscript //nologo slmgr.vbs /ipk QFFDN-GRT3P-VKWWX-X7T3R-8B639 >nul&goto server) else wmic os | findstr /I "home" >nul
if %errorlevel% EQU 0 (cscript //nologo slmgr.vbs /ipk TX9XD-98N7V-6WMQ6-BX7FG-H8Q99 >nul&cscript //nologo slmgr.vbs /ipk 3KHY7-WNT83-DGQKR-F7HPR-844BM >nul&cscript //nologo slmgr.vbs /ipk 7HNRX-D7KGG-3K4RQ-4WPJ4-YTDFH >nul&cscript //nologo slmgr.vbs /ipk PVMJN-6DFY6-9CCP6-7BKTT-D3WVR >nul&goto server) else wmic os | findstr /I "education" >nul
if %errorlevel% EQU 0 (cscript //nologo slmgr.vbs /ipk NW6C2-QMPVW-D7KKK-3GKT6-VCFB2 >nul&cscript //nologo slmgr.vbs /ipk 2WH4N-8QGBV-H22JP-CT43Q-MDWWJ >nul&goto server) else wmic os | findstr /I "10 pro" >nul
if %errorlevel% EQU 0 (cscript //nologo slmgr.vbs /ipk W269N-WFGWX-YVC9B-4J6C9-T83GX >nul&cscript //nologo slmgr.vbs /ipk MH37W-N47XK-V7XM9-C7227-GCQG9 >nul&goto server) else (goto notsupported)
:server
if %i% GTR 10 goto busy
if %i% EQU 1 set KMS=s8.uk.to
if %i% EQU 2 set KMS=s9.uk.to
if %i% EQU 3 set KMS=kms7.MSGuides.com
if %i% EQU 4 set KMS=kms8.MSGuides.com
if %i% EQU 5 set KMS=kms9.MSGuides.com
if %i% GTR 5 goto ato
cscript //nologo slmgr.vbs /skms %KMS%:1688 >nul
:ato
echo ============================================================================&echo.&echo.&cscript //nologo slmgr.vbs /ato | find /i "successfully" && (echo.&echo ============================================================================&echo.&echo #Dukung kami agar cara ini bisa terus digunakan!&echo #Like, Comment, Share dan Subscribe https://youtube.com/@ontachannel&echo #Terima kasih atas dukungan anda!&echo.&echo ============================================================================& if errorlevel 2 exit) || (echo Sepertinya butuh waktu lebih, silahkan tunggu... & echo. & echo. & set /a i+=1 & goto server)&explorer "https://blog-onta.blogspot.com/search/label/microsoft"&goto halt
:notsupported
echo ============================================================================&echo.&echo Maaf, windows 10 anda tidak support.&echo.&goto halt
:busy
echo ============================================================================&echo.&echo Server sedang sibuk, sedang mencoba lagi, silahkan tunggu...&echo.&set /a i=1&goto server
:halt
cd %~dp0&del %0 >nul&pause >nul
