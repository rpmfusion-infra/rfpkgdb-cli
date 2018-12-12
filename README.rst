=======================
RPMFusion PackageDB-cli
=======================

:Maintainer: FeRD (Frank Dana)
:Contact: ferdnyc@gmail.com
:Date: Wed Dec 12 2018
:Version: 2.15.0_rc1
:Author: Pierre-Yves Chibon <pingou@fedoraproject.org>

The `rfpkgdb-cli` is a commande line interface to the PackageDB of RPMFusion.

.. contents::

-------
Project
-------

The `PackageDB-cli` was started in May of 2011 to allow user to consult the
package collection and to manage their Access Control List (ACL) using a simple
interface web free interface.

.. _`PackageDB-cli`: https://fedorahosted.org/packagedb-cli

As of 2014, this project has been ported to
`pkgdb2 <https://github.com/fedora-infra/pkgdb2>`_. At this occasion, it is
has been re-written to propose a python module to query pkgdb2 API as well
as the pkgdb2client.cli module containing the command line interface and the
pkgdb2client.admin module containing a command line interface for admins to
interact with `pkgdb2`_.

In December 2018 the package was forked and adopted at rpmfusion as
`rfpkgdb-cli` after being orphaned at Fedora, as it is still used
with various RPMFusion infra tools and needed to be converted for
Python 3 compatibility.

------------
Installation
------------


Install Prerequisites
~~~~~~~~~~~~~~~~~~~~~

::

  dnf install python-fedora


Get and Run the Source
~~~~~~~~~~~~~~~~~~~~~~~~

* Install python-virtualenvwrapper

::

  dnf install python-virtualenvwrapper rpmfusion-cert

* Create the virtual environment

::

  mkvirtualenv rfpkgdb-cli --system-site-packages

* Activate the virtual environment

::

  workon rfpkgdb-cli

* Get the project

::

  git clone http://github.com/rpmfusion-infra/rfpkgdb-cli.git
  cd rfpkgdb-cli

* Set up the project

::

  python setup.py develop

* Run pkgdb-cli or pkgdb-admin

::

  python rfpkgdb2client/cli.py
  python rfpkgdb2client/admin.py

