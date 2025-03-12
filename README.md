# FH-Wels-Thesis-Template

This is a re-created template for writing scientific texts and theses at the University of Applied Sciences Upper Austria - Campus Wels. It may be freely used by anyone outside of that institution as well.

Deviation from these instructions is permitted, but support will not be provided for non-standard modifications.

## Features

Improvements over the provided version from FHOOE:

- Faster compilation
  - Particularly beneficial for Overleaf (free tier has a 20s compile limit)
- Backwards compatibility with the provided template (to be verified)
- Default TikZ support (TODO)
  - Template for continuous plots (TODO)
  - Template for discrete plots (TODO)

## Prerequisites

This template requires the following software:

- TeX Live
- TeXstudio
- GitHub Desktop

To effectively use this template, familiarity with TeX/LaTeX is necessary. Basic knowledge of Git and KOMA-Script is recommended. Many solutions found online may not work correctly with KOMA-Script.

When seeking AI-generated assistance (e.g., ChatGPT, Copilot), specify that you are using KOMA-Script or the `scrbook` document class. As of February 2025, GitHub Copilot with the Claude Sonnet Model is recommended for LaTeX help.

TeX Live is preferred over MiKTeX due to faster compilation and broader package support. This guide assumes a Windows system; official support for Linux and macOS is not provided.

For German users, this [YouTube Playlist](https://www.youtube.com/playlist?list=PL0FqMC_xCtjTg5XgHXhNPUJNib6gW_Zpi) serves as a reference. The recommended TeXstudio settings align with those in the playlist, but follow the installation instructions here instead. Whether to use `de_DE`, `de_AT`, or another dictionaries in TeXstudio is up to the user. If dictionaries are unavailable, check [this resource](https://tex.stackexchange.com/questions/87650/dictionary-for-texstudio-no-dictionary-available).

See the [Extended Playlist](https://www.youtube.com/playlist?list=PL0FqMC_xCtjTEasZqICLLwTjk80rAP2GQ) for further guidance.

Links to English TeX resources will be added soon.

## Installation

Installation time varies, but plan for at least three hours. Avoid using university WiFi; install at home instead. All software must be installed in English.

### TeX Live

Download the [TeX Live installer](https://mirror.ctan.org/systems/texlive/tlnet/install-tl-windows.exe) and run it. If prompted with "Windows protected your PC," click `More info`, then `Run Anyway`.

In the TeX Live installer:

1. Close both windows
2. Click the Windows icon and search for `TLShell TeX Live Manager`; (see tip below for alternatives)
3. Open it and wait for it to establish a connection
4. Click `All` (should show many packages)
5. Click `Not installed` (should show no packages; otherwise, install all)
6. Click `Updateable` (should show no packages; otherwise, update all)
7. Close the manager

>[!tip]
>If `TLShell` does not appear in Windows search, open `cmd` and type `tlshell`. Alternatively, navigate to `C:\texlive\2024\bin\windows\tlshell.exe` (adjust year if needed) and create a desktop shortcut.

### MiKTeX

TeX Live is recommended, but MiKTeX can be used if preferred. Note that TeX Live compiles 20-30% faster and has better package support. 

>[!warning]
>Do not install more than one TeX distribution.

### TeXstudio

Installation options:

- Open PowerShell (preferably as admin) and run:

  ```powershell
  winget install texstudio.texstudio --locale en-US
  ```

- Alternatively, download from [texstudio.org](https://www.texstudio.org/) and install manually.

Set the language to English. Other settings can remain at default.

### GitHub Desktop

Installation options:

- Use PowerShell (preferably as admin) and run:
  
  ```powershell
  winget install github.githubdesktop --locale en-US
  ```

- Alternatively, download from [github.com](https://desktop.github.com/) and install manually.

Set the language to English.

## Configuration

### GitHub Desktop

1. Create a [GitHub account](https://github.com/) (use a private email, not a university/work address).
2. In GitHub Desktop:
3. Visit the [GitHub repository](https://github.com/Gugarutz/FH-Wels-Thesis-Template) or scroll to the top
4. Click `<> Code` > `Open with GitHub Desktop`
5. Click allow in the browser pop
6. A popup in GitHub Desktop will open
7. Set the local path to `C:\Github\[reponame]`

>[!Important]
> Do not use long directory paths or OneDrive folders to avoid syncing issues. Use a separate backup solution (e.g., FreeFileSync) for replication to a cloud folder or external storage.

To manually download the template:

1. Visit the [GitHub repository](https://github.com/Gugarutz/FH-Wels-Thesis-Template)
2. Click `<> Code` > `Download ZIP`
3. Extract to `C:\Github\[reponame]`

Ensure the file structure is not nested:

```bash
C:\Github\[reponame]\thesis.tex
```

Delete `README.md`, `LICENSE.md`, and `.gitignore` if not using Git.

### TeXstudio Configuration

Run `Biber` under `Tools > Commands > Biber`.

## Using Git and GitHub Desktop

- Make small, documented commits
- Commit selectively, especially for non-text elements (plots, graphics, tables)
- Before modifying anything, create a branch for the original template
- Create a new branch for writing your thesis
- Leave the main branch as a reference
- If you rename the thesis.pdf, make sure to adjust the .gitignore file
  - Git and binary files (here: PDFs) do not mix

## Using the Template

The main file is `thesis.tex`. Set it as root manually or by opening `thesis.txss2` from GitHub Desktop or File Explorer.

The template is modular for faster compilation. Disable unused modules by commenting out `\input[modulename]` under `MODULES`. 

Use `\include{}` for chapters and sections. Use `\input` for everything else, it is a "dumb" 
Use `\includeonly{}` to only compile selected sections for faster compiles.


First, compile the template. Check the `Log` below for errors, warnings, or info messages. Save a copy of `thesis.pdf` as `template.pdf` for reference.

### First Steps

#### Data Entry

Edit `preamble/titlepage-data.tex` with relevant details.

#### Digital Signature

Enable/disable the digital signature in `preamble/signature.tex` by following the instructions in the comments.

#### Language Selection

Set language after `\begin{document}`:

- Use `\selectlanguage{}` (options: `english`, `ngerman`, `naustrian`)
- Choose `\titlepageDE` or `\titlepageEN`
- Select `\input{preamble/declarationDE}` or `\input{preamble/declarationEN}`
- Set the locale for `\sisetup`
- Provide both English and German abstracts

>[!note]
 Do not delete template code; comment it out instead.

[//]: # "chatticus: Consider adding additional documentation for advanced features like bibliography management, table formatting, and custom styling."
