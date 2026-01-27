Requirements and Setup
======================

- ✅ Install and configure compilers
- ✅ Configure Python environment
- ✅ Test f2py


Install and configure compilers
-------------------------------

Compiler Requirements:
- ``Windows:`` `C Compiler: MSVC (mandatory)` and `Fortran Compiler: Intel OneAPI`
    - Installation Order:
        - First: Install MSVC
        - Second: Install Intel OneAPI

- ``Linux/macOS:`` `C Compiler: gcc` and `Fortran Compiler: gfortran`


Configure Python environment
----------------------------    

Python Requirements:
- Windows: Python == 3.11
- Linux/macOS: Python >= 3.11 <= 3.13
- Required: pip and numpy.f2py


Test f2py
---------

Cube4Health is a Python package developed using version 3.10, which provides a set of scripts for processing and publishing data related to health, climate, and drone imagery, with a specific focus on the Brazilian context. The package follows protocols defined within each module, enabling the integration and analysis of data from various sources, provided they comply with these protocols. It offers an efficient solution for handling such data, facilitating the extraction of essential information for monitoring public health, climate change, and other environmental variables that impact population well-being.

