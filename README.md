# Interface between the Windows OS and Dyalog APL


`WinSys` is a member of the APLTree library. The library is a collection of classes etc. that aim to support the Dyalog APL programmer. Search GitHub for "apltree" and you will find solutions to many every-day problems Dyalog APL programmers might have to solve.


## Overview

`WinSys` offers methods that are useful for getting information regarding the Windows operating system.

Note that there is also a class `OS` which aims to offer methods you want to have on all supported platforms (Windows, Linux, Mac OS) like getting the process ID of the current process or killing a process etc.


## Methods
 
 | **Name** | **Remark** |
 |----------|------------|
 | `CONSTANT` | Creates a niladic function that returns a fixed result. |
 | `CreateParms_ShellExecute` | Creates a namespace with default values for `ShellExecute`.|
 | `ExpandEnv` | Expands Windows envirnment variables like `PATH`.|
 | `FindExecutable` | Returns the executable that would process `⍵` (existing filename). |
 | `FindWindow` | Returns a handle to a Window in case ⍵ matches the caption.|
 | `GetAllDrives` | Returns all drive letters for the current system.|
 | `GetComputerName` | |
 | `GetDiskFreeSpace` | |
 | `GetDPI` | Returns the current setting of DPI like 100 (default), 125 or 150. |
 | `GetDriveAndType` | Returns matrix with 2 cols: letter and type ("Fixed”, “CD-ROM”, ...|
 | `GetFormCaptionFontInfo` | Tells the font used by Windows for form captions.|
 | `GetHandleFromCaption` | Alias for `FindWindow`. |
 | `GetLastError` | |
 | `GetModuleFileName` | Helps to find out which DLLs were really loaded. |
 | `GetMsgFrom` | Takes an error number and returns the associated text.|
 | `GetProcessID`  | (deprecated; see the `OS` class) |
 | `GetSystemMetrics` | Useful to retrieve all sorts of information about Windows.|
 | `GetSystemParametersInfo` | Returns the "SystemParametersInfo" structure.|
 | `GetVersion` | Get the version of the OS. |
 | `GetWindowsDirectory` | |
 | `IsRunningAsAdmin` | |
 | `KillProcess` | (deprecated; see the `OS` class) |
 | `List_SM` | Returns a list with field names with names that start with `SM_`.|
 | `SetWindowParms` | Useful to set "Posn" or "Size" etc. for a window we have a handle for.|
 | `ShellExecute` | Deprecated. See the `OS` class.|
 | `Version` | Returns a 3-item vector with name, version number and version date.|

## Constants

|Name                        | Meaning                                |
|----------------------------|----------------------------------------|
|SM_CXSCREEN                 |Screen size                             |
|SM_CYSCREEN                 |                                        |
|SM_CXVSCROLL                |Vertical scroll bar width               |
|SM_CYVSCROLL                |Vertical scroll bar arrow bitmap height |
|SM_CXHSCROLL                |Horizontal scroll bar arrow bitmap width|
|SM_CYHSCROLL                |Horizontal scroll bar height            |
|SM_CYCAPTION                |Window title height of with frame       |
|SM_CXBORDER←                |2D window border size                   |
....