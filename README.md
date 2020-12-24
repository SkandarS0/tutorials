**Applying a display language even for a Home Edition single language:**
> _Maybe your desired language is already installed but not selected._
    
   1- First check installed language packs on your computer.
   Press `Win+R` and type cmd, then press `ctrl+shift+enter` to Command Prompt as an Administrator.
>
   2- Type `dism /online /get-packages` and press `enter`.
> _We are looking for **Microsoft-Windows-Client-LanguagePack-Package** as a start for **Package Identity**. And its State should be **Installed** as [this image](https://i.stack.imgur.com/FoP0c.png)._

> You can see next 5 characters after _~_ for understanding which language it is.
> In this example, we are seeing **tr-TR**. If you are looking for English for example, you should look for **en-US**.

> **If you found the desired language go to step 4. Otherwise, continue to step 3.**

 3- Downloading the desired display language:

   1- Visiting https://uupdump.ml/

   2- Searching for keywords of your Win10 build. For example, System Information showed my Win10 was at version 10.0.18363, build 18363, so I entered "18363 amd64"

   3- Clicking on a Cumulative update of your build in the search results

   4- In Search files, search for "languagepack"

   5- Downloading the .esd file of the language pack you wish to use
    
   6- Rename the downloaded file with just adding .esd at the end of it.

   7- Converting the .esd file into a .cab file. 
> _You can use this tool for example [ESD2CAB-CAB2ESD](https://github.com/abbodi1406/WHD/blob/master/scripts/ESD2CAB-CAB2ESD.zip) .
It has a readme explaining how to use it._
