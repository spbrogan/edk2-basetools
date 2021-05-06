# Publishing Tianocore Edk2 BaseTools (edk2basetools)

The __edk2basetools__ is published as a pypi (pip) module.  The pip module is named __edk2-basetools__.  Pypi allows for easy version management, dependency management, and sharing.

Publishing/releasing a new version is generally handled thru a server based build process but for completeness the process is documented here.

## Version Scheme

Versioning follows: aa.bb.cc and is based on tags in git

* aa == Major version.  Changes don’t need to be backward compatible
* bb == Minor version.  Significant new features.  Backward compatibility generally maintained except when new feature is used.
* cc == Patch version.  Bug fix or small optional feature.  Backward compatibility maintained.

## Publishing Process

1. Pass all development tests and checks.
2. Update the __readme.md__ `Release Version History` section with info on all important changes for this version.  Remove the "-dev" tag from the version about to be released.
3. Get your changes into main branch (official releases should only be done from the main branch)
4. Make a git tag for the version that will be released and push tag.  Tag format is v\<Major>.\<Minor>.\<Patch>
5. Do the release process

    1. Install tools
        ``` cmd
        pip install --upgrade -r requirements.publisher.txt
        ```
    2. Build a wheel
        ``` cmd
        python setup.py sdist bdist_wheel
        ```
    3. Confirm wheel version is aligned with git tag
        ``` cmd
        ConfirmVersionAndTag.py
        ```
    4. Publish the wheel/distribution to pypi
        ``` cmd
        twine upload dist/*
        ```
