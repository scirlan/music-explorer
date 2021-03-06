Music Explorer
==============

Music Explorer is a Nokia Developer example application demonstrating the use of
Nokia Music API together with standard Windows Phone 8 audio features to create
an immersive music experience. It shows how to take advantage of Nokia Music API
features such as searching for artists by name and requesting top artists and
new releases, and it also shows how to launch Nokia Music application from
within another application to play mix radio or show artist/product information.  

The example has been developed with Silverlight for Windows Phone devices
and tested to work on Nokia Lumia devices with Windows Phone 8.

This example application is hosted in GitHub:
https://github.com/nokia-developer/music-explorer

For more information on implementation and porting, visit Nokia Lumia
Developer's Library:
http://developer.nokia.com/Resources/Library/Lumia/#!code-examples/music-explorer.html


1. Usage
-------------------------------------------------------------------------------

This is a simple build-and-run solution. Learn about what you can do with Nokia 
Music API related features by trying out the application. 


2. Prerequisites
-------------------------------------------------------------------------------

* C# basics
* Windows 8
* Microsoft Visual Studio Express for Windows Phone 2012
* NuGet 2.1 (https://nuget.org/), Visual Studio extension to install and update
  third-party libraries and tools in Visual Studio


3. Project structure and implementation
-------------------------------------------------------------------------------

3.1 Folders
-----------

* The root folder contains the project file, the license information and this
  file (release_notes.txt).
* `MusicExplorer`: Root folder for the implementation files.  
* `Assets`: Graphic assets like icons and tiles.
* `Properties`: Application property files.
* `Resources`: Application resources.
* `Models`: `MainViewModel` and models to bind data and user interface.

3.2 Important files and classes
-------------------------------

| File | Description |
| ---- | ----------- |
| `ArtistPage.xaml` | The page showing artist specific info in a pivot component. |
| `ArtistPage.xaml.cs` | The code-behind file of the artist page. |
| `MainPage.xaml` | The main page of the application with the panorama component. |
| `MainPage.xaml.cs` | The code-behind file of the main page. |
| `MusicApi.cs` | Class responsible of communicating with the Nokia Music API. |
| `MainViewModel.cs` | Binds data and user interface.  |

| Class | Description |
| ----- | ----------- |
| `ArtistPage` | This class handles almost half of the UI. |
| `MainPage` | This class handles almost half of the UI. |
| `MainViewModel` | This class is responsible for binding the data and UI together. |
| `MusicApi` | This class is responsible for all the communication to Nokia Music API. |

3.3 Used APIs/Windows Phone Components
--------------------------------------

* Microsoft.Phone.Maps.Services
* Microsoft.Phone.Controls.Toolkit
* Microsoft.Xna.Framework
* Microsoft.Xna.Framework.Media
* Newtonsoft.Json
* Nokia.Music.Wp8
* System.Device.Location
* Windows.Devices.Geolocation


4. Compatibility
-------------------------------------------------------------------------------

* Windows Phone 8

Tested to work on Nokia Lumia 920 and Nokia Lumia 1520. 
Developed with Microsoft Visual Studio Express for Windows Phone 2012.

4.1 Required Capabilities
-------------------------

* `ID_CAP_LOCATION`
* `ID_CAP_MAP`
* `ID_CAP_MEDIALIB_AUDIO`
* `ID_CAP_MEDIALIB_PLAYBACK`
* `ID_CAP_NETWORKING`
* `ID_CAP_SENSORS`

4.2 Known Issues
----------------

None.


5. Building, installing, and running the application
-------------------------------------------------------------------------------

5.1 Preparations
----------------

Make sure you have the following installed:
 * Windows 8
 * Windows Phone SDK 8.0
 * Latest NuGet Package Manager (>2.7.1) from https://nuget.org/ to enable 
   NuGet Package Restore

5.2 Using the WINDOWS PHONE 8 SDK
---------------------------------

1. Open the SLN file:
   File > Open Project, select the file MusicExplorer.sln
2. Select the target 'Emulator WXGA'.
3. Press F5 to build the project and run it on the Windows Phone Emulator.

5.3 Deploying to Windows Phone 8
--------------------------------

Please see official documentation for deploying and testing applications on
Windows Phone devices:
http://msdn.microsoft.com/en-us/library/gg588378%28v=vs.92%29.aspx


6. License
-------------------------------------------------------------------------------

    Copyright � 2013 Nokia Corporation. All rights reserved.
    
    Nokia, Nokia Developer, and HERE are trademarks and/or registered trademarks of
    Nokia Corporation. Other product and company names mentioned herein may be
    trademarks or trade names of their respective owners.
    
    License
    Subject to the conditions below, you may use, copy, modify and/or merge copies
    of this software and associated content and documentation files (the �Software�)
    to test, develop, publish, distribute, sub-license and/or sell new software
    derived from or incorporating the Software, solely in connection with Nokia
    devices. Some of the documentation, content and/or software maybe licensed under
    open source software or other licenses. To the extent such documentation,
    content and/or software are included, licenses and/or other terms and conditions
    shall apply in addition and/or instead of this notice. The exact terms of the
    licenses, disclaimers, acknowledgements and notices are reproduced in the
    materials provided, or in other obvious locations. No other license to any other
    intellectual property rights is granted herein.
    
    This file, unmodified, shall be included with all copies or substantial portions
    of the Software that are distributed in source code form.
    
    The Software cannot constitute the primary value of any new software derived
    from or incorporating the Software.
    
    Any person dealing with the Software shall not misrepresent the source of the
    Software.
    
    Disclaimer
    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
    FOR A PARTICULAR PURPOSE, QUALITY AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES (INCLUDING,
    WITHOUT LIMITATION, DIRECT, SPECIAL, INDIRECT, PUNITIVE, CONSEQUENTIAL,
    EXEMPLARY AND/ OR INCIDENTAL DAMAGES) OR OTHER LIABILITY, WHETHER IN AN ACTION
    OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
    SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
    
    Nokia Corporation retains the right to make changes to this document at any
    time, without notice.


7. Related documentation
-------------------------------------------------------------------------------

"Nokia Music API" documentation published on Nokia Lumia Developer's Library
(http://www.developer.nokia.com/Resources/Library/Lumia/#!nokia-music-api.html) 
describes the properties and usage of Nokia Music API in detail.

�Optimising for Nokia phablets� documentation on Nokia Lumia Developer's Library
(http://developer.nokia.com/Resources/Library/Lumia/#!optimising-for-nokia-phablets.html)
describes how to optimize applications for large screen, different aspect 
ratios, and multiple resolutions. 

8. Version history
-------------------------------------------------------------------------------

* 1.1.0.0 Major UI-rework (new tile based design replacing list based design,
          utilizing images of higher resolution in 1080p devices and NuGet 
          package restore support.
* 1.0.1.0 Bug fix to handle exception when location is set off
* 1.0.0.0 First release
* 0.4.0.0 Minor fixes
* 0.3.0.0 Public beta
