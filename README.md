# FH-Wels-Thesis-Template

![Contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen)
![GitHub issues](https://img.shields.io/github/issues/Gugarutz/FH-Wels-Thesis-Template)

This is a re-created template for writing scientific texts and theses at the University of Applied Sciences Upper Austria - Campus Wels. It may be freely used by anyone outside of that institution as well.

Deviation from these instructions is permitted, but support will not be provided for non-standard modifications.

![PDFLaTeX](https://img.shields.io/badge/PDFLaTeX-Required-blue)

## Features

Improvements over the provided version from FHOOE:

- Faster compilation
  - Particularly beneficial for Overleaf (free tier has a 20s compile limit)
- Backwards compatibility with the provided template (to be verified)
- Default TikZ support (TODO)
  - Template for continuous plots (TODO)
  - Template for discrete plots (TODO)

## Prerequisites

This assumes the following software:

![TeX Live](https://img.shields.io/badge/TeX%20Live-Recommended-blue)
![TeXstudio](https://img.shields.io/badge/TeXstudio-Recommended-blue)
[![GitHub Desktop](https://img.shields.io/badge/GitHub%20Desktop-Recommended-blue)](https://desktop.github.com/)

See [## Recommended setup] for installation.

To effectively use this template, familiarity with TeX/LaTeX is necessary. Basic knowledge of Git and KOMA-Scrips is recommended. Many solutions found online may not work correctly with KOMA-Script.

TeX Live is preferred over MiKTeX due to faster compilation and broader package support. This guide assumes a Windows 10/11 system; official support for GNU+Linux and OSX is not provided. The recommended install should work fine with either.

### German Users

For German users, this [YouTube Playlist](https://www.youtube.com/playlist?list=PL0FqMC_xCtjTg5XgHXhNPUJNib6gW_Zpi) serves as a reference. The recommended TeXstudio settings align with those in the playlist, but follow the installation instructions here in case of conflicting information.

See the [Extended Playlist](https://www.youtube.com/playlist?list=PL0FqMC_xCtjTEasZqICLLwTjk80rAP2GQ) for a deeper understanding of TeX. Highly recommended.

Whether to use `de_DE`, `de_AT`, or another dictionaries for spellchecking in TeXstudio is up to the user. The spellchecking can be changed at any time in the bottom right and can be inserted as a [magic comment](https://texstudio-org.github.io/advanced.html#advanced-header-usage) for each file (per file spellcheck).
If dictionaries are unavailable, check this resource: [TeXstudio Dictionary Issue](https://tex.stackexchange.com/questions/87650/dictionary-for-texstudio-no-dictionary-available)

### English Users

>[!important] Help wanted
>Links to english resources.

The [official TeXstudio decumentation](https://texstudio-org.github.io/getting_started.html) is a good reference, but maybe not be a good learining resource.

### Use of AI & chat bots

When seeking AI-generated assistance (e.g., ChatGPT, Copilot), specify that you are using KOMA-Script or the `scrbook` document class. As of February 2025, GitHub Copilot with the *Claude Sonnet* Model is recommended for LaTeX help.

TeXstudio can have integrated AI help. See the official [TeX studio documentation](https://texstudio-org.github.io/advanced.html#ai-chat-assistant) for setup.

## Recommended setup

Installation time varies, but plan for at least three hours. Avoid using university WiFi; install at home instead. All software must be installed in English.

<details>

### TeX Live

Download the [TeX Live installer](https://mirror.ctan.org/systems/texlive/tlnet/install-tl-windows.exe) and run it. If prompted with "Windows protected your PC," click `More info`, then `Run Anyway`.

>[!note]Author's comment
> Yes, I know this install sucks, I do not like it either. But trust me here and use TeX Live if you can.

In the TeX Live installer:

1. Close both windows
2. Click the Windows icon and search for `TLShell TeX Live Manager`; (see tip below for alternatives)
3. Open it and wait for it to establish a connection
4. Click `All` (should show many packages)
5. Click `Not installed` (should show no packages; otherwise, install all)
6. Click `Updateable` (should show no packages; otherwise, update all)
7. Close the manager

>[!tip]
>If `TLShell TeX Live Manager` does not appear in Windows search, open `cmd` and type `tlshell`.
>
>Alternatively, navigate to `C:\texlive\2024\bin\windows\tlshell.exe` (year may vary) and create a desktop shortcut.

### Install TeXstudio & GitHub Desktop

Using winget:

- Open PowerShell (preferably as admin) and run:

``` bash
winget install texstudio.texstudio --locale en-US
```

``` bash
winget install github.githubdesktop --locale en-US
```

Using standard Windows installation:

- Download from [texstudio.org](https://www.texstudio.org/) and install manually. Set the language to **English**, other settings can remain at default.
- Download from [github.com](https://desktop.github.com/) and install manually.

Set the language to English.

### Configure GitHub Desktop

1. Create a [GitHub account](https://github.com/) (use a private email, not a university/work email).
2. In GitHub Desktop:
3. Visit the [GitHub repository](https://github.com/Gugarutz/FH-Wels-Thesis-Template) or scroll to the top
4. Click `<> Code` > `Open with GitHub Desktop`
5. Click allow in the browser pop up
6. A popup in GitHub Desktop will open
7. Set the local path to `C:\Github\[reponame]`

>[!Important]
> Do not use long directory paths or OneDrive folders to avoid syncing issues. Use a separate backup solution (e.g., FreeFileSync) for replication to a cloud folder or external storage.

</details>

## Alternative setup (no Admin rights)

The alternative setup uses MikTeX and VSCode as these can be installed per user instead of system wide. Therefore not needing admin rights. The system provided to you in your internship will likely not have admin rights.

TeX Live is recommended, but MiKTeX can be used if preferred. Note that TeX Live compiles 20-30% faster and has better package support.

>[!warning]
>Currently, I cannot provide you with any information or help for this setup.
>
>You will need to install the relevant extensions for TeX in VSCode yourself. (Help is appreciated)

>[!warning]
>Installing Git requires admin rights. You can use VSCode for writing and GitHub Desktop for commiting. Consider Overleaf.

### Install MikTeX & VS Code

<details>

  Open `cmd` or `powershell` and run:

  ``` bash
  winget install MikTeX.MikTeX --locale en-US
  ```

  Then run:

  ``` bash
  winget install vscode --locale en-US
  ```

  >[!warning]
  >Do not install more than one TeX distribution. (mostly for your own sanity)

</details>

## Using Git and GitHub Desktop

- Make small, documented commits
- Commit selectively, especially for non-text elements (plots, graphics, tables)
- Before modifying anything, create a branch for the original template
- Create a new branch for writing your thesis
- Leave the main branch as a reference
  - this will facilitate easier rebasing/merging (updating the code)
- If you rename the main.pdf, make sure to adjust the .gitignore file
  - Git and binary files (here: PDFs) do not mix

## Overleaf & ZIP download

An Overleaf project for easier setup will be provided soon.

[![Overleaf](https://img.shields.io/badge/Overleaf-Open-green)](https://www.overleaf.com/read/kwxdfrpxsvyy#9f071f)


To manually download the template:

1. Visit the [GitHub repository](https://github.com/Gugarutz/FH-Wels-Thesis-Template)
2. Click `<> Code` > `Download ZIP`
3. To work locally:
   1. Extract to `C:\Github\`
   2. Ensure the file structure is not nested:

    ```path
    C:\Github\[reponame]\main.tex
    ```

4. To use Overleaf
   1. Create a new (Blank) project
   2. Upload the ZIP-file to Overleaf (need to check if this works)
   3. Ensure `main.tex` is at the root of the structure (outside any folder)
5. Delete `LICENSE`, `.gitignore`, `.gitattributes`, `main.txss2`, they are not needed.
6. Keep the `README.md` as a reference

## Using the Template

The template is modular for faster compilation. Disable unused modules by commenting out `\input{[modulename]}` under `%% MODULES`.

- Use `\include{}` for chapters and sections, it automatically adds a `\clearpage`. It cannot be nested. It cannot be used in the preamble.
- Use `\input` for everything else, it is "dumb", it does not do anything other than a directly inserting your code.
- Use `\includeonly{}` to only compile selected sections for faster compiles.

>[!tip]
> Use `\clearpage` instead of `\newpage`, it clears all floats (tables, figures, etc.).
>
> **Only create manual page breaks when absolutely necessary!** Let LaTeX work.

First, compile the template. Check the `Log` below for errors, warnings, or info messages. Save a copy of `main.pdf` as `template.pdf` for reference.

### First Steps

The main file is `main.tex`. Set it as root manually or by opening `main.txss2` from GitHub Desktop or File Explorer.

Run `Biber` under `Tools > Commands > Biber`. You may need to rerun this occasionally.

#### Data Entry

Edit `preamble/titlepage-data.tex` with relevant details.

#### Digital Signature

Enable/disable the digital signature in `preamble/signature.tex` by following the instructions in the comments.

#### Language Selection

Set language after `\begin{document}`:

- Use `\selectlanguage{}` (options: `english`, `ngerman`, `naustrian`)
- Choose `\titlepageDE` or `\titlepageEN`
- Choose `\declarationDE` or `\declarationEN`
- Set the locale for `\sisetup`
- Provide both English and German abstracts

>[!note]
> Never delete template code; comment it out instead. This way you can keep it as a reference. Feel free to delete the `\include{ch-demo/...}` chapters, sections and appendices.

## About this repository

A quick overview of this repository.

### Contributing

Contributions are welcome! But please make Pull Requests with the relevant fixes ONLY. No other changes, e.g. "I did some code formatting in a completely different file while I was fixing a bug with TikZ". Changing the documentation when changing the implementation of a feature is of course permitted and desired.

If there is a relevant issue that was fixed, please mark that.

### License

![License](https://img.shields.io/github/license/Gugarutz/FH-Wels-Thesis-Template)

The license does not cover the FHOOE logo, which is the property of the FHOOE.
