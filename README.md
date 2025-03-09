# FH-Wels-Thesis-Template
This a re-created template for writing scientific texts and thesis at the University of Applied Science Upper Austria - Campus Wels. It may be freely used by anyone outside of that as well.

Deviation to these instructions is of course permitted, I cannot stop you, but you will be on your own.
## Prerequisites
The template uses the following software/libraries as a basis:
* TeX Live
* TeX studio
* Github Desktop

To properly use this template, you must first understand how TeX or LaTeX works. Must also understand the fundamental ideas behind Github or Git in general. Basic knowledge of the KOMA scripts is recommended, you do not need to read all of almost 600 pages of the KOMA documentation. Many answers online work differently or not at all with KOMA.

When asking ChatGPT, Copilot or other similar, ensure to provide context that you are using KOMA or scrbook (the specific KOMA doucment class used here). As of February 2025 Github Copilot with the Claude Sonnet Model is recommended for LaTeX help. For research purposes it is you decicion.

Usage of other software is not supported. TeX Live is preferred over MikTex for faster compilation and wider package support. We will be working on a Windows system, there is no official support for Linux or Mac as of yet. 

For German users this [YouTube Playlist](https://www.youtube.com/playlist?list=PL0FqMC_xCtjTg5XgHXhNPUJNib6gW_Zpi) is taken as a basis. The settings for TeXstudio used here overlap with the ones set there. However, perform the installation as described here and not the way it is done in the tutorial. Whether you use de_DE or de_AT or any other language is up to you. Also exercise your way through the [Extended Playlist](https://www.youtube.com/playlist?list=PL0FqMC_xCtjTEasZqICLLwTjk80rAP2GQ).

@ -19,7 +21,7 @@ Links to English TeX resources will follow soon.
If no dictionaries are available check [here](https://tex.stackexchange.com/questions/87650/dictionary-for-texstudio-no-dictionary-available)

## Installation
The total time to install can vary a lot. Plan for at least 2 hours with a good internet connection, this is not due to the size of the installation but rather because it downloads all packages individually. Do *not* use the WiFi at the university, do this at home. The TeXLive installer takes its time. All software is to be installed in ENGLISH.

### TeX Live
Start by downloading the [install-tl-windows.exe](https://mirror.ctan.org/systems/texlive/tlnet/install-tl-windows.exe) directly through this link or from [here](https://mirror.ctan.org/systems/texlive/tlnet) if you are using a different OS. Double click the exe file in you downloads folder. Windows will prompt you that "Windows protected your PC", click `More info` then `Run Anyway`.
@ -40,27 +42,48 @@ In the TeX Live installer:
9. Close both windows
10. Click the Windows icon in the lower left
11. And search for `TLShell TeX Live Manager`
12. Open it*
12. Wait for it to establish a connection
13. Click on `All`; you should see many packages
14. Click on `Not installed`; you should see no packages. Otherwise install all
14. Click on `Updateable`; you should see no packages. Otherwise Update all
15. Close the  manager

We are done here.

[NOTE] If Windows search does not find the TLShell, open a cmd window (search for cmd, open), and type `tlshell`. This will open the 
[NOTE] If this fails too, head to or paste `C:\texlive\2024\bin\windows\tlshell.exe`. The year may vary. You may want to create a desktop shortcut for future use.

### MikTex
I cannot enforce the usage of TeXLive. You can use MikTex if you are not comfortable with the TeXLive website or the install process. It *should* work just fine. Know that TeXLive is 20-30% faster during compilation, which will save you a lot of time in the long run. It also has support for more packages.

### TeXstudio
This install is simple. You can either
- open powershell, preferrably as admin
- `winget install texstudio.texstudio`
- while you are here, you can skip ahead:
- `winget install github.githubdesktop`

or 

- head to [texstudio.org](https://www.texstudio.org/)
- Click the big `Download now` button
- Click through the installer
- **set the language to English**. German is not supported and not recommended
- Leave everything to the default settings otherwise

### Github Desktop
This install is also simple. You can use `winget install github.githubdesktop` or head to their [website](https://desktop.github.com/). Same as TeXstudio: Click the big `Download` button and click through the installer. Leave everything to the default settings but **set the language to English**. German is not supported here.

## Configuration
We will need to configure TeXstudio and Github for us to be able to use it properly and fully.

### Github (Desktop)
Create a [Github](https://github.com/) account. Use your private email address, do not use the university or work/internship address. You will not have access to them after leaving those institutions.


%%%%%%%%%%%%%%%%% this needs a rewrite
In Github Desktop: 
* Click `File > New Repository`
* Choose a name and ensure compliance
* Choose a description if you like
@ -68,7 +91,7 @@ In Github Desktop:
* Ensure `initialise this repository with a README` is checked off
* Ensure `License` and `Gitignore` are set to `none`

[Note] IMPORTANT: Choose `C:\Github` as your directory. **Do not use long directory paths or especially OneDrive folders.** This will lead to syncing issues with any other systems and will cause a lot of syncing from OneDrive. You may still use a cloud service for backing up your work. Look into FreeFileSync for automatic replication of your thesis to a cloud folder or other medium (e.g. USB stick, external hard drive).

Now head to the [Github repo of this template](https://github.com/Gugarutz/FH-Wels-Thesis-Template.git) or scroll up. Click the bright green button that says `<> Code` and click `Download ZIP`. It will download to your usual download folder, navigate the and extract the files to your new repo in `C:\Github\[reponame]`. Ensure the result is NOT 
```
@ -83,21 +106,84 @@ Now go back to Github Desktop. You should see all the new files in the left pane

On the lower left, give this version (commit) a name in the summary field. You may call this "original" or "base" for example. Click on `commit to main` and `Push origin` in the centre pane. Only this last part actually uploads to Github.

### Overleaf or not using Github Desktop

While this is very much not recommended, it is up to you. If you have not admin rights on the PC/laptop you have at work/intership, you can use [Overleaf](https://www.overleaf.com). ensure to extract
 
Now head to the [Github repo of this template](https://github.com/Gugarutz/FH-Wels-Thesis-Template.git) or scroll up. Click the bright green button that says `<> Code` and click `Download ZIP`. It will download to your usual download folder, navigate the and extract the files to your new repo in `C:\Github\[reponame]`. Ensure the result is **not** something like this:
```
C:\Github\[mainfolder]\FH-Wels-Thesis-Template\thesis.tex	or
C:\Github\[mainfolder]\FH-Wels-Thesis-Template-main\thesis.tex
```
Ensure a shallow directory, like this:
```
C:\Github\[mainfolder]\thesis.tex
C:\[mainfolder]\thesis.tex
```
The same goes if you are using Overleaf, ensure that thesis.tex is at the very front and not in a subfolder.

[NOTE] delete the README.md LICENSE.md and .gitignore files, if not using Git. They will be unused


### TeXstudio

% Biber 

## using Git and Github Desktop
Since you will be using this alone, you do not need to fuss about with git too much.
- When working on your thesis, make small and local commits, this way you will be able to go back to very specific points if things break
- Document each commit at least somewhat
- choose what to include in each commit
- this is especially crucial for non text parts, like plots, tables, graphics
- **before you start changing anything create a branch for the original template**
- Work in the main branch or the 
- This way you can switch between the template and your thesis very quickly for troubleshooting
- I know you are not taking this seriously and will be lazy with git

[NOTE] Github Copilot online chat can currently (February 2025) only access the main branch when feeding it a repo.

## Using the template
See Prerequisites for the assumed basics of using TeX and Git. 

Ensure Github Desktop is open.
The `thesis.tex` file is the main file

The template is built in a modular way for faster compilation. If you do not need some features like native LaTeX plots via TikZ/PGF or source code formatting, feel free to disable these `\input{modulename}` under the `MODULES` section. Make sure to exclude the example code from the structure, otherwise it will not compile. For long works or generally faster compiles, check the usage of the `\includeonly{}` command.



Close TS if it is currently opened. Open `thesis.txss2` from Github Desktop or the file explorer. This will set the `thesis.tex` file as the root file, so it does not matter which file you have open when you compile, you can even close `thesis.tex`. This will also set the open tabs and panes. If you wish to restore the order simply reopen the session file through `File > Session > Load`. You can also save a session and overwrite the one provided, the root document will be saved again.



First of all, compile the template. Check the `Log` at the bottom. There should be no errors, warnings, infos. Create a copy of the `thesis.pdf` and rename it to `template.pdf` or whatever suits you. Keep this copy as quick reference. 
### First steps
From here you can also switch to the documentation provided by the template directly. The first few steps are also laid out here.

[NOTE] A word of advice: Do not delete any code provided by the template. Comment it out.

#### Data
Find and right-click on `\input{preamble/titlepage-data}` in `thesis.tex` and click Open. Fill out all the data. You can do this later as well, of course. Alternatively, open via file system.

#### digital signature
To enable or disable displaying the digital signature:
- Open `/preamble/signature.tex`
- Follow instructions in comment up top

#### language selection
All language selection is made after `\begin{document}`. No selection/changes need to be made in the preamble.

- right after `\begin{document}` is `\selectlanguage{}`, choose from english, ngerman or naustrian. The *n* stands for *new* as in *new grammar*.
- Next choose between `\titlepageDE` and `\titlepageEN`
- Next choose between `\input{preamble/declarationDE}` and `\input{preamble/declarationEN}`
- You need both English and German abstract
- Some chapter and section headings are for you to change, like the Preface

[NOTE]
- you can use `\selectlanguage{}` whenenver switching languages inside the document
- Do not forget to switch back, or use the group functionality
- This is used in the two abstract files
- {the contents inside loose curly brackets (meaning not part of a command) are a group}
---

