.. _temi:

=======
Themes
=======

Sphinx supports changing the appearance of its HTML output via **themes**. A theme is a collection of HTML templates, stylesheets and other static files.

The default theme for a Sphinx project is *Alabaster*, but there are plenty of free themes that you can choose. Here you can find some: https://sphinx-themes.org.


Exercise: Change the theme of your Sphinx project
-------------------------------------------------

Suppose that you've browsed `Sphinx themes <https://sphinx-themes.org>`__ and you've chosen `Read the docs <https://sphinx-themes.org/sample-sites/sphinx-rtd-theme/>`__ theme for your project. These few steps will show you how to install and use it.

Change the theme locally
~~~~~~~~~~~~~~~~~~~~~~~~

*   **Step 1**: install the theme locally.

In your shell, run:

.. code-block:: shell

	pip install sphinx-rtd-theme

*   **Step 2**: edit ``conf.py`` file.

Open ``conf.py``, look for the ``html_theme`` variable end edit as follows:

.. code-block:: python

	html_theme = 'sphinx_rtd_theme'

*   **Step 3**: build.

Build your documentation and enjoy your new theme locally.


Change the theme in GitHub and GitLab pages
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

*   **Step 1**: edit ``.yml`` files.

** 	For GitHub, you have to edit the ``documentation.yml`` file. In order to install the theme, edit line 16 of the file (see :ref:`here <github>`) with the following:

.. code-block:: shell

	 pip install sphinx sphinx_rtd_theme myst_parser sphinx-rtd-theme

**  For GitLab, you have to edit the ``.gitlab-ci.yml`` file. In order to install the theme, add the following line in the file, before both ``sphinx-build`` commands (see :ref:`here <gitlab>`):

.. code-block:: shell

  - pip install sphinx-rtd-theme


*   **Step 2**: edit ``conf.py`` file.

Open ``conf.py``, look for the ``html_theme`` variable end edit as follows:

.. code-block:: python

	html_theme = 'sphinx_rtd_theme'

*   **Step 3**: push the changes to your repository.

The deployment will start automatically and the webpage will be rendered with the new theme.