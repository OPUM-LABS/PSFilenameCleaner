# PSFilenameCleaner

<div id="top"></div>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]



<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/OPUM-LABS/PSFilenameCleaner/">
    <img src="/.gitignore/strong-language_l-blue.png" alt="Logo" width="100" height="100">
  </a>

<h3 align="center">PSFilenameCleaner</h3>

  <p align="center">
    Remove unwanted or invalid characters in your filenames.
    <br />
    <br />
    <a href="https://github.com/OPUM-LABS/PSFilenameCleaner/issues">Report Bug</a>
    ·
    <a href="https://github.com/OPUM-LABS/PSFilenameCleaner/pulls">Request Feature</a>
  </p>
</div>


<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#features">Features</a></li>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
          <ul>
        <li><a href="#gui-mode">GUI-Mode</a></li>
        <li><a href="#detached-mode">Detached-Mode</a></li>
      </ul>
    <li><a href="#license">License</a></li>
  </ol>
</details>


<!-- ABOUT THE PROJECT -->
## About The Project

[![Product Name Screen Shot][product-screenshot]](https://github.com/OPUM-LABS/PSFilenameCleaner/blob/main/.gitignore/Screenshot_PSFilenameCleaner.png)

This program allows you to remove or replace all unwanted symbols/characters from your files with just one click.  
You can set your own filter based on your needs.

### Features
You can do for all selectet users at once:  
✨ Remove or replace all unwanted symbols/characters from your files with one click  
✨ Select individual files or whole folders (inclusive subfolders)  
✨ Works recursive through all subfolders  
✨ Keep one or more symbols/characters  
✨ GUI and detached mode (e.g. as a scheduled task)   

### Built With

* [PowerShell Studio 2022](https://www.sapien.com/software/powershell_studio)
* [Windows PowerShell](https://docs.microsoft.com/en-us/powershell/)
* [Windows PowerShell ISE](https://docs.microsoft.com/en-us/powershell/scripting/windows-powershell/ise/introducing-the-windows-powershell-ise?view=powershell-7.1)
* [Notepad++](https://notepad-plus-plus.org/)
<p align="right">(<a href="#top">back to top</a>)</p>

<!-- GETTING STARTED -->
## Getting Started

Just download the latest PSFilenameCleaner.exe or PSFilenameCleaner.ps1.  
(Note that neither the EXE nor the PS1 file is signed.  
A warning message will appear either when you download the file(s) or most likely later when you try to open it!)

### Prerequisites

The following prerequisites must be met:
* PowerShell 5 and up

### Installation

This is a program/script that can be easily run without installation.
<p align="right">(<a href="#top">back to top</a>)</p>


<!-- USAGE EXAMPLES -->
## Usage
(It goes without saying that you must also have the necessary rights to the files to rename them)
### GUI-Mode
1. Open PSFilenameCleaner.ps1 (right-click "Run with PowerShell") or PSFilenameCleaner.exe
2. Select your file(s) or directory that cointains your files you want to "clean"
3. Set your filter based on the ASCII-Table (mouseover to show the table)  
(For compatibility reasons I don't recomment to set te upper limit to a higher number than 127)
4. Set the symbols/characters you want to keep
5. Set the symbols/characters you want to replace the incompatible ones with
6. Click on "Run"

### Detached-Mode
(Only works with PSFilenameCleaner.**ps1**)
#### Parameters
| Parameter    | Type     | Mandatory | Default Value | Description                                                    |
|--------------|----------|-----------|---------------|----------------------------------------------------------------|
| -Help        | [switch] | no        | $false        | Displays the help page.                                        |
| -Detached    | [switch] | no        | $false        | Run this script in the background.                             |
| -SourceDir   | [string] | yes*      | -             | Define the source folder (recursive) or the source file.       |
| -LogDir      | [string] | yes*      | -             | Define the directory where the log files should be written to. |
| -ASCIIStart  | [int]    | no        | 0             | Define the first index number of the ASCII-Table.              |
| -ASCIIEnd    | [int]    | no        | 127           | Define the last index number of the ASCII-Table.               |
| -AllowChar   | [string] | no        | -             | Define all allowed characters.                                 |
| -ReplaceChar | [string] | no        | -             | Define the replace characters.                                 |

*Only mandatory when executed in detached mode (-Detached)!

#### Examples
- Run with just mandatory parameters (source = directory):
```powershell
.\PSFilenameCleaner.ps1 -Detached -SourceDir "C:\tmp\source" -LogDir "C:\tmp\logs"
```
- Run with just mandatory parameters (source = file):
```powershell
.\PSFilenameCleaner.ps1 -Detached -SourceDir "C:\tmp\source\file.txt" -LogDir "C:\tmp\logs"
```
- Run with all parameters:
```powershell
.\PSFilenameCleaner.ps1 -Detached -SourceDir "C:\tmp\source" -LogDir "C:\tmp\logs" -ASCIIStart "12" -ASCIIEnd "32" -AllowChar "€©" -ReplaceChar "-"
```
<p align="right">(<a href="#top">back to top</a>)</p>


<!-- LICENSE -->
## License

Distributed under the GNU General Public License v3.0. See `LICENSE` for more information.
<p align="right">(<a href="#top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/OPUM-LABS/PSFilenameCleaner.svg?style=for-the-badge
[contributors-url]: https://github.com/OPUM-LABS/PSFilenameCleaner/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/OPUM-LABS/PSFilenameCleaner.svg?style=for-the-badge
[forks-url]: https://github.com/OPUM-LABS/PSFilenameCleaner/network/members
[stars-shield]: https://img.shields.io/github/stars/OPUM-LABS/PSFilenameCleaner.svg?style=for-the-badge
[stars-url]: https://github.com/OPUM-LABS/PSFilenameCleaner/stargazers
[issues-shield]: https://img.shields.io/github/issues/OPUM-LABS/PSFilenameCleaner.svg?style=for-the-badge
[issues-url]: https://github.com/OPUM-LABS/PSFilenameCleaner/issues
[license-shield]: https://img.shields.io/github/license/OPUM-LABS/PSFilenameCleaner.svg?style=for-the-badge
[license-url]: https://github.com/OPUM-LABS/PSFilenameCleaner/blob/master/LICENSE
[product-screenshot]: .gitignore/Screenshot_PSFilenameCleaner.png
