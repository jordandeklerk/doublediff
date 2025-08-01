============
Installation
============

Installing moderndid
---------------------

.. tip::

    This page assumes you are comfortable using a terminal and are familiar with package managers.
    The only prerequisite for installing moderndid is Python itself. If you don't have Python yet and want
    the simplest way to get started, we recommend you use the Anaconda Distribution - it includes Python,
    NumPy, and many other commonly used packages for scientific computing and data science.
    You can download Anaconda from `here <https://www.anaconda.com/download>`_.

The recommended method of installing moderndid depends on your preferred workflow. Below, we break down the installation methods
into the following categories:

- Installing from PyPI
- Installing from conda-forge
- Installing from source

Choose the method that best suits your needs. If you're unsure, start with the Environment-based method using ``conda`` or ``pip``.

The two main tools that install Python packages are ``pip`` and ``conda``. Their functionality partially overlaps (e.g. both can install moderndid),
however, they can also work together. We'll discuss the major differences between pip and conda here - this is important to understand if
you want to manage packages effectively.

The first difference is that conda is cross-language and it can install Python, while pip is installed for a particular Python on your system
and installs other packages to that same Python install only. This also means conda can install non-Python libraries and tools you may need
(e.g. compilers, CUDA, HDF5), while pip can't.

The second difference is that pip installs from the Python Packaging Index (PyPI), while conda installs from its own channels
(typically "defaults" or "conda-forge"). PyPI is the largest collection of packages by far, however, all popular packages are available for conda as well.

The third difference is that conda is an integrated solution for managing packages, dependencies and environments, while with pip you
may need another tool (there are many!) for dealing with environments or complex dependencies.

- **Conda**: If you use conda, you can install moderndid from the conda-forge channel by creating a new environment and installing moderndid:

.. code-block:: console

    conda create -n my-env
    conda activate my-env
    conda install moderndid

- **pip**: If you use pip, you can install moderndid from PyPI:

.. code-block:: console

    pip install moderndid

- **Development**: To install the latest development version from GitHub:

.. code-block:: console

    pip install git+https://github.com/jordandeklerk/moderndid

.. tip::

    Use a virtual environment for better dependency management.

.. code-block:: console

    python -m venv my-env
    source my-env/bin/activate  # macOS/Linux
    my-env\Scripts\activate     # Windows
    pip install moderndid

Verifying the installation
---------------------------

To verify that moderndid is installed correctly, you can run the following command:

.. code-block:: console

    python -c "import moderndid; print(moderndid.__version__)"

Development
-----------

To install moderndid for development:

.. code-block:: console

    git clone https://github.com/jordandeklerk/moderndid.git
    cd moderndid
    pip install -e ".[dev]"

This will install moderndid in editable mode along with all development dependencies.
