# IO Data Analysis *TheRa.py*

## Introduction

This repository is a collection of code and data used in IO *TheRa.py Sessions*, the informal series of workshops tailored for the proteomics researcher struggling to take those first steps into data analysis with R (and eventually Python). 

To set up a data analysis environment using R, RStudio, and RTools. Follow the steps below to get started.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Downloading and Installing R](#downloading-and-installing-r)
- [Downloading and Installing RStudio](#downloading-and-installing-rstudio)
- [Compiling Packages from Source](#compiling-packages-from-source)
- [Getting Started](#getting-started)

## Prerequisites

Before you begin, ensure you have the following:

- A computer with internet access
- Administrative access to install software

## Downloading and Installing R

R is a free software environment for statistical computing and graphics.

### Windows:

1. Go to the [CRAN R project download page](https://cran.rstudio.com/).
2. Click on the "Download R for Windows" link.
3. Click on "base" and then click on the "Download R <version number> for Windows" link to download the installer.
4. Run the installer and follow the on-screen instructions.

### macOS:

1. Follow [this link](https://cran.rstudio.com/bin/macosx/) to the R download page for macOS
2. Determine the architecure of your Mac's chip. Open System Settings > General > About > Chip.
   - If your Mac has an Apple chip, click the download link containing `arm64.pkg`.
   - If your Mac has an Intel chip, click the download link containing `x86_64.pkg`.
3. If your browser asks if it is okay to download from the current website, allow.
4. By default the `.pkg` installer will download to your "Downloads" folder; open Finder > Downloads and double click the `.pkg` file you just downloaded.
5. Follow the on-screen instructions to install R. If your Mac prompts you to allow any permissions, allow.

## Downloading and Installing RStudio

RStudio is an integrated development environment (IDE) for R that provides a user-friendly interface for running and managing R code.

### Windows and macOS:
1. Go to the [RStudio download page](https://posit.co/download/rstudio-desktop/).
2. Under the "2: Install RStudio" section, click the download link for your operating system (Windows or macOS).
   - If the link doesn't match your operating system, scroll down to "All Installers and Tarballs" and select the appropriate version.
3. Install.
   - On macOS:
      - Again, the program will, by default, be downloaded to your "Downloads" folder.
      - Unlike before, this program is downloaded as a `.dmg` file (Disk Image). To install R Studio, double click the `.dmg` file. Then, in the new view that appears, drag the R Studio icon to the "Applications" folder shortcut.
   - On Windows:
     - Once the installer is downloaded, run it and follow the on-screen instructions.

## Compiling Packages from Source

To compile R packages from source, you need to install the necessary development tools. This is particularly useful if you want to install the latest versions of packages, or if binary versions are not available for your operating system. Some R packages contain C, C++, or Fortran code that needs to be compiled into machine code to run efficiently. By compiling from source, you can ensure compatibility and potentially gain performance improvements.

### Why Compiling from Source is Necessary

1. **Access to Latest Features and Fixes**: Some packages may have newer versions available that contain important bug fixes or new features. These updates may not yet be available in precompiled binary formats. This is common in research computing.
2. **Compatibility**: Certain packages or systems might not have precompiled binaries available, especially on less common operating systems. Building from source ensures you can still use these packages.

### Compiling Packages on Windows (Rtools)

Rtools is a collection of tools necessary for building R packages on Windows.

1. Go to the [Rtools download page](https://cran.r-project.org/bin/windows/Rtools/).
2. Download the appropriate version of Rtools corresponding to your R version. (i.e. "Rtools44 installer")
3. Run the installer and follow the on-screen instructions.
4. In the R console (see RStudio) run `Sys.which("make")` and see if it finds a `make.exe` file. If so, you're good to go. If not, proceed to the next step. 
4. Add Rtools to your system PATH:
    - Open the "System Properties" window by right-clicking on "This PC" and selecting "Properties."
    - Click on "Advanced system settings" and then on the "Environment Variables" button.
    - Under "System variables," find the "Path" variable, select it, and click "Edit."
    - Click "New" and add the path to the Rtools `bin` directory (e.g., `C:\Rtools\bin`).

### Compiling Packages on macOS

To compile R packages from source on macOS, you only need to install Xcode Command Line Tools:

1. Open a Terminal window.
   - You may find this program by clicking the Spotlight Search icon (magnifying glass) in your menu bar, then search for “Terminal”.
   - Otherwise, it can be found in Finder > Applications > Utilities
2. Copy and paste the following into the terminal, then press enter: `sudo xcode-select --install`. You may need to input your password. (If so, no characters will appear.)
3. Follow any onscreen instructions and wait for it to finish.

You can now compile R packages!

## Getting Started

Once you have installed R, RStudio, and Rtools:

1. Open RStudio.
2. You can start writing R code in the script editor or console.
3. Explore the various features and tools, such as the environment pane, plots, and packages pane.
