<<<<<<< HEAD
# OSeMOSYS user interface is open source web/standalone web app for creating model solution with OSeMOSYS
MUIO is an open source modelling system for long-run integrated assessment and energy planning.
WebApp javascript
API flask python 3
=======
# Modelling User Interface for OSeMOSYS (MUIO)
>>>>>>> c738e7c65a0f46c5824e450d6555f5b91b918dc7

![License](https://img.shields.io/github/license/OSeMOSYS/MUIO)
![Version](https://img.shields.io/github/v/release/OSeMOSYS/MUIO)
![GitHub all releases](https://img.shields.io/github/downloads/OSeMOSYS/MUIO/total)

This repository contains the user interface for the Open Source Energy Modelling System (OSeMOSYS). OSeMOSYS is a linear optimization energy system model designed to minimize total system costs while ensuring energy demands are met within specified constraints. It facilitates optimal allocation of energy resources, technologies, and investments over time, supporting long-term energy planning and policy analysis.

<<<<<<< HEAD
#####################################################################################################
In order for MUIO to solve problem created with UI you will need to download GLPK and COIN CBC solver.
In development environment in folder WebAPP\SOLVERs create two folders named COIN-OR and GLPK.
In COIN-OR folder unpack exactly this version of CBC binaries Cbc-2.7.5-win64-intel11.1.
In GLPK folder unpack version glpk-4.65.
Folder tree for CBC should look like WebAPP\SOLVERs\COIN-OR\Cbc-2.7.5-win64-intel11.1\bin
and for GLPK WebAPP\SOLVERs\GLPK\glpk-4.65\w64.
=======
# Introduction

Energy system modelling is essential for making well-informed decisions in energy planning. Many existing models and interfaces for comprehensive energy studies are either cost-prohibitive or require extensive programming skills, limiting accessibility. MUIO emerges as a powerful solution to these challenges, offering both open access and a user-friendly interface with a quick learning curve.

Built on top of the OSeMOSYS code, MUIO enables users to construct and calibrate energy system models of basic to intermediate complexity. It allows for the representation of complete energy chains—from primary energy sources through supply systems to final demand sectors. Additionally, MUIO enhances efficiency by enabling users to run models locally and evaluate multiple scenarios simultaneously, streamlining the entire modelling process and making it more practical for a wide range of applications.

# Installation

1.	Download the latest version of the user interface from [here](https://forms.office.com/Pages/ResponsePage.aspx?id=wE8mz7iun0SQVILORFQISwwn5YyR7ONHs-3JdG3f5AFUODlJOEQwWTBXMlRRNFUwNEpUTUZYQ1RXOS4u). 
2.	Move the .exe file from your download folder to a folder where you have administrator privileges. This may be for instance inside the folder: users>>name_of_the_user or any other folder you prefer. 
3.	Right-click on MUIO.exe and click ‘Run as administrator’. This will start the installation of the MUIO. The installation may take several minutes. Once it is complete, the installation window will simply disappear. 
4.	The App will open automatically once the installation is complete. If not, search on the Windows Taskbar for ‘’MUIO’’ and open the App. 
5.	You will see the MUIO in a new window. 

## Questions and Issues

For troubleshooting model-related issues and discussions, please visit the [Energy Modelling Community Discussion Forum](https://forum.u4ria.org/). 

If you encounter bugs or have new feature ideas, please submit them to the repository's issue tracker. We encourage contributions and discussions to further develop MUIO.
>>>>>>> c738e7c65a0f46c5824e450d6555f5b91b918dc7
