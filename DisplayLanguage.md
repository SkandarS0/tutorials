**Applying a display language even for a Home Edition single language:**
> _Maybe your desired language is already installed but not selected._

> First, check installed language packs on your computer.

   **1- Press `Win+R` and type cmd, then press `ctrl+shift+enter` to Command Prompt as an Administrator.**
   
   **2- Type `dism /online /get-packages` and press `enter`.**
> _We are looking for **Microsoft-Windows-Client-LanguagePack-Package** as a start for **Package Identity**. And its State should be **Installed** as [this image](https://i.stack.imgur.com/FoP0c.png)._

> You can see next 5 characters after _~_ for understanding which language it is.
> In this example, we are seeing **tr-TR**. If you are looking for English for example, you should look for **en-US**.

> **If you found the desired language go to step 5. Otherwise, continue to step 3.**

 **3- Downloading the desired display language:**

   a- Visiting [uupdump Website](https://uupdump.ml/).

   b- Searching for keywords of your Windows 10 Build Version.
   
> For example, System Information showed my OS Build Version **19042.685**, so I entered _**19042.685**_ as [this image](https://github.com/tightropeboy/saved/blob/main/Screenshot%202020-12-24%20224632.jpg?raw=true)
   
   c- Clicking on a Cumulative update of your build in the search results

   d- In Search files, search for "languagepack"

   e- Downloading the .esd file of the language pack you wish to use
    
   f- Rename the downloaded file with just adding .esd at the end of it.

   g- Converting the .esd file into a .cab file. 
> _You can use this tool for example for step 1-g [ESD2CAB-CAB2ESD](https://github.com/abbodi1406/WHD/blob/master/scripts/ESD2CAB-CAB2ESD.zip) .
It has a readme explaining how to use it._

 **4- Installing the desired display Language:**
 
   a- Open the Command Prompt again as an administrator.
    
   b- Type `dism /online /add-package /packagepath:C:\lp.cab` .
    
>**Instead of _C:\lp.cab_ you have to type the absolute path of the _.cab_ file and then paste the name of the _.cab_ with its extension `.cab`**
    
   c- Press `enter` .
   
   d- Wait for the installation to be finished.
   
 **5- Applying :heavy_check_mark::**
    
   a- Press `Win+R`, type `regedit`, press `ctrl+shift+enter` for the Administrative rights.
   
   b- Navigate to `\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Language`.
   
> Default entry shows that language id of your system.

   c- Check this [link](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c?redirectedfrom=MSDN) to look for your desired language ID from list and Copy the part after 0x part.
   
> For example check [this](https://i.stack.imgur.com/idMMr.png), for en-US, get 0409.

   d- Double-click on **Default** to change its value to the desired language ID, same for **InstallLanguage**'s value.
   
   e- Exit the registry editor and restart.
