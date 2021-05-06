# Tianocore Edk2 Python BaseTools (edk2basetools)

This is a Tianocore maintained project consisting of a the python source files that make up EDK2 basetools. This package's intent is to provide an easy way to organize and share python code to facilitate reuse across environments, tools, and scripts.  Inclusion of this package and dependency management is best managed using Pip/Pypi.

This is a fundamental package and is required to be used for edk2 builds.

## Current Status

| Host Type | Toolchain | Branch | Build Status | Test Status | Code Coverage |
| :-------- | :-------- | :---- | :----- | :---- | :--- |
| Linux Ubuntu 20.04 | Python 3.9.x | main | [![Build Status](https://dev.azure.com/tianocore/edk2-basetools/_apis/build/status/CI%20-%20Ubuntu?branchName=main)](https://dev.azure.com/tianocore/edk2-basetools/_build/latest?definitionId=56&branchName=main) | ![Azure DevOps tests](https://img.shields.io/azure-devops/tests/tianocore/edk2-basetools/56.svg) | ![Azure DevOps coverage](https://img.shields.io/azure-devops/coverage/tianocore/edk2-basetools/56.svg) |
| Windows Server 2019 | Python 3.9.x | main | [![Build Status](https://dev.azure.com/tianocore/edk2-basetools/_apis/build/status/CI%20-%20Windows?branchName=main)](https://dev.azure.com/tianocore/edk2-basetools/_build/latest?definitionId=54&branchName=main) | ![Azure DevOps tests](https://img.shields.io/azure-devops/tests/tianocore/edk2-basetools/54.svg)| ![Azure DevOps coverage](https://img.shields.io/azure-devops/coverage/tianocore/edk2-basetools/54.svg) |

### Current Release

[![PyPI](https://img.shields.io/pypi/v/edk2-basetools.svg)](https://pypi.org/project/edk2-basetools/)

All release information is now tracked with Github
 [tags](https://github.com/tianocore/edk2-basetools/tags),
 [releases](https://github.com/tianocore/edk2-basetools/releases) and
 [milestones](https://github.com/tianocore/edk2-basetools/milestones).

## How to use it for building Tianocore based projects

### Basic usage

In general this should be transparent for you.  Assuming you already have a virtual environment
for your edk2 repo and you already pip install the *pip-requirements.txt file* then it is up to 
your build environment to use the correct binwrappers. 

In the tianocore/edk2 repo this is handled by the *BaseTools/toolsetup.bat* or the pytool based 
descriptors (see BaseTools/BinWrappers/WindowsLike/win_build_tools_path_env.yaml).  These methods
will use the version installed in your python environment so managing that version is outside
the scope of this readme.

### Development usage or tools debugging

Because the repos are configured to use the installed version it is just a matter of installing the version
you want.  Python, pip, and virtual environments make this easy.  

1. Clone the repo locally
2. Check out the version you want and/or make local changes
3. Open cmd prompt and activate the virtual environment you plan to use for building
4. Run `pip install -e .` from the folder you cloned into
5. Build your edk2 based project using the same virtual environment

## License

All content in this repository is licensed under [BSD-2-Clause Plus Patent License](license.txt).

[![PyPI - License](https://img.shields.io/pypi/l/edk2-basetools.svg)](https://pypi.org/project/edk2-basetools/)

## Contribution Process

This project welcomes all types of contributions.
For issues, bugs, and questions it is best to open a [github issue](https://github.com/tianocore/edk2-basetools/issues).

### Code Contributions

For code contributions this project leverages github pull requests.  See github tutorials, help, and documentation for complete descriptions.
For best success please follow the below process.

1. Contributor opens an issue describing problem or new desired functionality
2. Contributor forks repository in github
3. Contributor creates branch for work in their fork
4. Contributor makes code changes, writes relevant unit tests, authors documentation and release notes as necessary.
5. Contributor runs tests locally
6. Contributor submits PR to main branch of tianocore/edk2-basetools
    1. PR reviewers will provide feedback on change.  If any modifications are required, contributor will make changes and push updates.
    2. PR automation will run and validate tests pass
    3. If all comments resolved, maintainers approved, and tests pass the PR will be squash merged and closed by the maintainers.

## Maintainers

See the [github team](https://github.com/orgs/tianocore/teams/edk-ii-tool-maintainers) for more details.

## Documentation

See the github repo __docs__ folder
