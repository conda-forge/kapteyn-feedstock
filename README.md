About kapteyn
=============

Home: https://www.astro.rug.nl/software/kapteyn/

Package license: BSD 3-Clause

Feedstock license: BSD 3-Clause

Summary: Astronomical package for spatial and spectral coordinates, WCS projections and transformation, and more...

The Kapteyn Package is a collection of Python modules and applications
developed by members of the computer group (*) of the Kapteyn
Astronomical Institute, University of Groningen, The Netherlands.  The
purpose of the package is to provide tools for the development of
astronomical applications with Python.

The package is suitable for both inexperienced and experienced users and
developers and documentation is provided for both groups.  The
documentation also provides in-depth chapters about celestial
transformations and spectral translations.

Some of the package's features:

   * The handling of spatial and spectral coordinates, WCS projections
     and transformations between different sky systems.  Spectral
     translations (e.g., between frequencies and velocities) are supported
     and also mixed coordinates.  (Modules wcs and celestial. Module wcs
     uses Mark Calabretta's WCSLIB which is distributed with the package.)

   * Versatile tools for writing small and dedicated applications for
     the inspection of FITS headers, the extraction and display of (FITS)
     data, interactive inspection of this data (color editing) and for the
     creation of plots with world coordinate information.  (Module maputils)
     As one example, a gallery of all-sky plots is provided.

   * A class for the efficient reading, writing and manipulating simple
     table-like structures in text files.  (Module tabarray)

   * Utilities for use with matplotlib such as obtaining coordinate
     information from plots, interactively modifiable colormaps and timer
     events (module mplutil); tools for parsing and interpreting coordinate
     information entered by the user (module positions).

   * A function to search for gaussian components in a profile
     (module profiles) and a class for non-linear least squares fitting
     (module kmpfit).


Current build status
====================

[![Linux](https://img.shields.io/circleci/project/github/conda-forge/kapteyn-feedstock/master.svg?label=Linux)](https://circleci.com/gh/conda-forge/kapteyn-feedstock)
[![OSX](https://img.shields.io/travis/conda-forge/kapteyn-feedstock/master.svg?label=macOS)](https://travis-ci.org/conda-forge/kapteyn-feedstock)
![Windows disabled](https://img.shields.io/badge/Windows-disabled-lightgrey.svg)

Current release info
====================

| Name | Downloads | Version | Platforms |
| --- | --- | --- | --- |
| [![Conda Recipe](https://img.shields.io/badge/recipe-kapteyn-green.svg)](https://anaconda.org/conda-forge/kapteyn) | [![Conda Downloads](https://img.shields.io/conda/dn/conda-forge/kapteyn.svg)](https://anaconda.org/conda-forge/kapteyn) | [![Conda Version](https://img.shields.io/conda/vn/conda-forge/kapteyn.svg)](https://anaconda.org/conda-forge/kapteyn) | [![Conda Platforms](https://img.shields.io/conda/pn/conda-forge/kapteyn.svg)](https://anaconda.org/conda-forge/kapteyn) |

Installing kapteyn
==================

Installing `kapteyn` from the `conda-forge` channel can be achieved by adding `conda-forge` to your channels with:

```
conda config --add channels conda-forge
```

Once the `conda-forge` channel has been enabled, `kapteyn` can be installed with:

```
conda install kapteyn
```

It is possible to list all of the versions of `kapteyn` available on your platform with:

```
conda search kapteyn --channel conda-forge
```


About conda-forge
=================

conda-forge is a community-led conda channel of installable packages.
In order to provide high-quality builds, the process has been automated into the
conda-forge GitHub organization. The conda-forge organization contains one repository
for each of the installable packages. Such a repository is known as a *feedstock*.

A feedstock is made up of a conda recipe (the instructions on what and how to build
the package) and the necessary configurations for automatic building using freely
available continuous integration services. Thanks to the awesome service provided by
[CircleCI](https://circleci.com/), [AppVeyor](http://www.appveyor.com/)
and [TravisCI](https://travis-ci.org/) it is possible to build and upload installable
packages to the [conda-forge](https://anaconda.org/conda-forge)
[Anaconda-Cloud](http://docs.anaconda.org/) channel for Linux, Windows and OSX respectively.

To manage the continuous integration and simplify feedstock maintenance
[conda-smithy](http://github.com/conda-forge/conda-smithy) has been developed.
Using the ``conda-forge.yml`` within this repository, it is possible to re-render all of
this feedstock's supporting files (e.g. the CI configuration files) with ``conda smithy rerender``.

For more information please check the [conda-forge documentation](https://conda-forge.org/docs/).

Terminology
===========

**feedstock** - the conda recipe (raw material), supporting scripts and CI configuration.

**conda-smithy** - the tool which helps orchestrate the feedstock.
                   Its primary use is in the construction of the CI ``.yml`` files
                   and simplify the management of *many* feedstocks.

**conda-forge** - the place where the feedstock and smithy live and work to
                  produce the finished article (built conda distributions)


Updating kapteyn-feedstock
==========================

If you would like to improve the kapteyn recipe or build a new
package version, please fork this repository and submit a PR. Upon submission,
your changes will be run on the appropriate platforms to give the reviewer an
opportunity to confirm that the changes result in a successful build. Once
merged, the recipe will be re-built and uploaded automatically to the
`conda-forge` channel, whereupon the built conda packages will be available for
everybody to install and use from the `conda-forge` channel.
Note that all branches in the conda-forge/kapteyn-feedstock are
immediately built and any created packages are uploaded, so PRs should be based
on branches in forks and branches in the main repository should only be used to
build distinct package versions.

In order to produce a uniquely identifiable distribution:
 * If the version of a package **is not** being increased, please add or increase
   the [``build/number``](http://conda.pydata.org/docs/building/meta-yaml.html#build-number-and-string).
 * If the version of a package **is** being increased, please remember to return
   the [``build/number``](http://conda.pydata.org/docs/building/meta-yaml.html#build-number-and-string)
   back to 0.