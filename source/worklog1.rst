

.. index:: worklog


====================
Working with Sphinx
====================



Change a Theme
================

#. Run ``pip install sphinx_rtd_theme`` to install the *Read The Docs* theme.
#. In the **conf.py** file, add ``html_theme = 'sphinx_rtd_theme'``.


Add a Logo Image
===================
#. Place the **logo.png** file to the ``source/_static`` folder.
#. In the **conf.py** file:

  - Add ``html_logo = './_static/logo.png'``.
  - Add the following argument:

::

	html_theme_options = {

    	'canonical_url': '',
    	'analytics_id': 'UA-XXXXXXX-1', #  Provided by Google in your dashboard
    	'logo_only': True,				#  Set as "True" to display logo only
    	'display_version': True,
    	'prev_next_buttons_location': 'bottom',
    	'style_external_links': False,
    	'vcs_pageview_mode': 'raw',
    	'style_nav_header_background': '#2980B9', 
    	'collapse_navigation': True,
    	'sticky_navigation': False,	
    	'navigation_depth': 4,
    	'includehidden': True,
    	'titles_only': False

	}


Insert a Table
================

Input
---------

.. image:: /_static/table.png


Result
---------

========= ==================================== ===========
Header A  Header B                             Header C
========= ==================================== ===========
A1        B1   								   C1
A2        B2       							   C2
========= ==================================== ===========


Insert an Image
================
#. Place the **picture.jpg** file to the ``source/_static`` folder.
#. Add ``.. image:: /_static/picture.jpg`` in the rst file.

