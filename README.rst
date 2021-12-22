.. image:: https://img.shields.io/badge/dmtn--212-lsst.io-brightgreen.svg
   :target: https://dmtn-212.lsst.io
.. image:: https://github.com/lsst-dm/dmtn-212/workflows/CI/badge.svg
   :target: https://github.com/lsst-dm/dmtn-212/actions/
..
  Uncomment this section and modify the DOI strings to include a Zenodo DOI badge in the README
  .. image:: https://zenodo.org/badge/doi/10.5281/zenodo.#####.svg
     :target: http://dx.doi.org/10.5281/zenodo.#####

##########################
The Rubin Science Platform
##########################

DMTN-212
========

The Rubin Science Platform (RSP) is a collection of services intended to provide the Rubin scientific community with "next-to-the-data" exploration and analysis capabilities. It refers to the major three user-facing aspects (Portal, Notebook, API) as well as the infrastructure services that support them.  Core user-facing services, infrastructure services as well as "guest" services all make use of a single cloud-native deployment infrastructure. 

This document describes the RSP system architecture, key technical decisions, a description of user-facing and supporting services, an explanation of the deployment infrastructure, and an outline of current operational environments. 

This is a live document describing existing capabilities as they are currently available as our system is continuously evolved to meet its design requirements as well as address future technical challenges and emerging user needs.

**Links:**

- Publication URL: https://dmtn-212.lsst.io
- Alternative editions: https://dmtn-212.lsst.io/v
- GitHub repository: https://github.com/lsst-dm/dmtn-212
- Build system: https://github.com/lsst-dm/dmtn-212/actions/


Build this technical note
=========================

You can clone this repository and build the technote locally with `Sphinx`_:

.. code-block:: bash

   git clone https://github.com/lsst-dm/dmtn-212
   cd dmtn-212
   pip install -r requirements.txt
   make html

.. note::

   In a Conda_ environment, ``pip install -r requirements.txt`` doesn't work as expected.
   Instead, ``pip`` install the packages listed in ``requirements.txt`` individually.

The built technote is located at ``_build/html/index.html``.

Editing this technical note
===========================

You can edit the ``index.rst`` file, which is a reStructuredText document.
The `DM reStructuredText Style Guide`_ is a good resource for how we write reStructuredText.

Remember that images and other types of assets should be stored in the ``_static/`` directory of this repository.
See ``_static/README.rst`` for more information.

The published technote at https://dmtn-212.lsst.io will be automatically rebuilt whenever you push your changes to the ``main`` branch on `GitHub <https://github.com/lsst-dm/dmtn-212>`_.

Updating metadata
=================

This technote's metadata is maintained in ``metadata.yaml``.
In this metadata you can edit the technote's title, authors, publication date, etc..
``metadata.yaml`` is self-documenting with inline comments.

Using the bibliographies
========================

The bibliography files in ``lsstbib/`` are copies from `lsst-texmf`_.
You can update them to the current `lsst-texmf`_ versions with::

   make refresh-bib

Add new bibliography items to the ``local.bib`` file in the root directory (and later add them to `lsst-texmf`_).

.. _Sphinx: http://sphinx-doc.org
.. _DM reStructuredText Style Guide: https://developer.lsst.io/restructuredtext/style.html
.. _this repo: ./index.rst
.. _Conda: http://conda.pydata.org/docs/
.. _lsst-texmf: https://lsst-texmf.lsst.io
