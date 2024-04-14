# FH-Wels-Thesis-Template
This a newly created template for writing scientific texts and thesis at the University of Applied Science Upper Austria - Campus Wels. It may be freely used by anyone outside of that as well.

Deviation to these instructions is of course permitted, but you will be on your own.
## Prerequisites
The template uses the following software/libraries as a basis:
* TeX Live
* TeX studio
* Github Desktop

To properly use this template, you must first understand how TeX or LaTeX works. Must also understand the fundamental ideas behind Github or Git in general. Basic knowledge of the KOMA scripts is recommended. Many answers online work differently or not at all with KOMA.

Usage of other software is not supported. TeX Live is preffered over MikTex for faster compilation and wider package support. We will be working on a Windows system, there is no support for Linux or Mac as of yet. 

For german users this [YouTube Playlist](https://www.youtube.com/playlist?list=PL0FqMC_xCtjTg5XgHXhNPUJNib6gW_Zpi) is taken as a basis. The settings for TeXstudio used here overlap with the ones set there. However, perform the insallation as described here and not the way it is done in the tutorial. Whether you use de_DE or de_AT or any other language is up to you. Also exercise your way through the [Extended Playlist](https://www.youtube.com/playlist?list=PL0FqMC_xCtjTEasZqICLLwTjk80rAP2GQ).

Links to English TeX resources will follow soon.

If no dictionaries are available check [here](https://tex.stackexchange.com/questions/87650/dictionary-for-texstudio-no-dictionary-available)

## Intallation
The total time to install can vary a lot. Plan for at least 2 hours with a decent internet connection (>50Mb/s). Do NOT use the WiFi at the university, do this at home. The TeX Live installer takes its time. All software is to be installed in ENGLISH.

### TeX Live
Start by downloading the [install-tl-windows.exe](https://mirror.ctan.org/systems/texlive/tlnet/install-tl-windows.exe) directly through this link or from [here](https://mirror.ctan.org/systems/texlive/tlnet) if you are using a different OS. Double click the exe file in you downloads folder. Windows will prompt you that "Windows protected your PC", click `More info` then `Run Anyway`.

In the TeX Live installer:

1. Ensure option `Install` is enabled. 
2. Click `Next`
3. Click `Install`
4. A second window will open
5. You may choose a mirror (location)
6. Or ignore, selecton will be automatic (recommended)
5. Ensure `Default paper size` is set to `A4`
6. Click `Install`
7. You may install the other software in the meantime
7. Let the installer finish (this is the long part)
8. Ensure it installed with no errors
9. Close both windows
10. Click the Windows icon in the lower left
11. And search for `TLShell TeX Live Manager`
12. Wait for it to establish a connection
13. Click on `All`; you should see many packages
14. Click on `Not installed`; you should see no packages. Otherwise install all
14. Click on `Upgradeable`; you should see no packages. Otherwise Upgrade all
15. Close the  manager

We are done here.

### TeXstudio
This install is simple. You can use `winget install texstudio` or head to [texstudio.org](https://www.texstudio.org/). Click the big `Download now` button and click through the installer. Leave everything to the default settings but SET THE LANGUAGE TO ENGLISH. German is not supported here.

### Github Desktop
This install is also simple. You can use `winget install github.githubdesktop` or head to their [website](https://desktop.github.com/). Same as TeXstudio: Click the big `Download` button and click through the installer. Leave everything to the default settings but SET THE LANGUAGE TO ENGLISH. German is not supported here.

## Configuration
We will need to configure TeXstudio and Github for us to be able to use it properly and fully.

### Github
Create a [Github](https://github.com/) account. Use your private email address, do not use the university or work/internship address. You will not have access to them after leaving those institutions.

In Github Desktop:
* Click `File > New Repository`
* Choose a name and ensure compliance
* Choose a description if you like
* Set the path to `C:\GitHub` [See note below]
* Ensure `initialise this repository with a README` is checked off
* Ensure `License` and `Gitignore` are set to `none`

[Note] IMPORTANT: Choose `C:\Github` as your directory. Do not use long directory paths or OneDrive folders. This will lead to syncing issues with any other systems and will cause a lot of syncing from OneDrive. You may still use a cloud service for backing up your work.

Now head to the [Github repo of this template](https://github.com/Gugarutz/FH-Wels-Thesis-Template.git) or scroll up. Click the bright green button that says `<> Code` and click `Download ZIP`. It will download to your usual download folder, navigate the and extract the files to your new repo in `C:\GitHub\[reponame]`. Ensure the result is NOT 
```
C:\GitHub\[reponame]\FH-Wels-Thesis-Template\thesis.tex	or
C:\GitHub\[reponame]\FH-Wels-Thesis-Template-main\thesis.tex
```
Ensure a flat directory, like this:
```
C:\GitHub\[reponame]\thesis.tex
```
Now go back to Github Desktop. You should see all the new files in the left pane. Click `Publish repository` at the top of the window. Ensure you have no mistakes in the name. Ensure your code will be kept private. Click `Publish repository`. 

On the lower left, give this version (commit) a name in the summary field. You may call this "original" or "base" for example. Click on `commit to main` and `Push origin` in the center pane. Only this last part actually uploads to Github.

### TeXstudio




## Using the template
See Prerequisites for the assumed basics of using TeX and Git. 

The template is built in a modular way for faster compilation and fewer errors/warnings. If you you need any additional features, check if they are implemented already, and enable them. 

Close TS if it is currently opened. Open `thesis.txss2` from Github Desktop or the file exlorer. This will set the `thesis.tex` file as the root file, so it does not matter whcih file you have open when you compile. this will also set the open tabs and panes. If you wish to restore the order 

Ensure GD is running in the background. 
The `thesis.tex` file is the main file

First of all right click on `\input{frontmatter/frontpage` and click Open. Fill out all the data 
