# pyKAN
PyKAN is a pure python alternative client for the CKAN utility to manage modules for Kerbal Space Program.
It uses the original upstream CKAN data and repos directly and does not fragment the module repositories,
it merely provides an alternate client to consume this data to manage, install and update modules.

All the logic is kept in libraries - so that writing a new interface is easy.

Version 0.1.0

##Installation:
1. Clone or Download the repository.
2. Change to the directory where you downloaded
3. Make sure you have python-requests and python-appdirs installed. The program will tell you if it cannot find these modules.
4. `./pyKAN --help`
5.   python pyKAN --help #On windows


##Current features:
1. Global settings holding list of known KSP installation directories
2. Per KSPDir settings on top of that
3. Fetch repository data from CKAN
4. Ability to install incompatible mods. Settings contain minKSPversion and maxKSPversion per install. By default these are set to the KSP version. User can override to, for example, allow mods that are maxed at 1.0.0 to install in 1.1.0.
5. List available modules. Module listing comes with numerous optional filters which can be combined in arbitrary combinations. Includes text-search, module version and KSP version compatibility. The same filters will be available for selecting mods to install.
6. Detect manually installed mods
7. Import list of modules installed by CKAN
8. List installed modules, indicating how they were installed. 
9. Install modules (optional override support for manual mods) with optional download-retries
10. Uninstall modules
11. Upgrade modules
12. Python3 - in master branch only.

##Changes
###0.1.0
1. The installed modules listing is now also sorted alphabetically.
2. Fixed a bug where calling upgrade would reinstall the same version as was there before
3. Disabled  strict mode JSON to deal with the bad json in .version files.
4. Handling of 'file' mode install sections now work correctly. 
5. Fixed install destination for mods like firespittercore
6. Use appdirs module to place main configuration file in a platform neutral manner

###0.0.1-beta2
1. Python3 support
2. Lots of small bugfixes
3. Improved mod installer, mod upgrades and mod uninstalls
4. List_module now sorts alphabetically

###0.0.1-beta1
1. Initial public release


##Todo:
1. PyQT GUI for graphical usage
2. Manual install by link. User can copy a download link and have the app download and install from within. User could add/edit mod information.
3. Optimize the O(N) and O(n*x) algorithms.
4. Improve the argument code for the commandline version. Some of it is a bit cumbersome.
5. ~~Import of CKAN installed list should also import filelist.~~ Done
6. Consider using a Linter for your source (I'd recommend flake8)
7. Consider using the logging module rather than a DEBUG flag
8. Consider documenting at all levels (package, module, class, function) using a known doc style (Plain, Epytext, restructuredText, Numpy, Google, etc.)
9. [very optional] Consider using type hints (a.k.a PEP 484) or even the typing module (see also PEP 526) if you switch to python3.

##Written By
1. A.J. Venter (metalpoetza on reddit).
2. SYZYGY - Python3 support

