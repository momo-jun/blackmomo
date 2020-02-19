

.. index:: worklog1


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

.. tip:: To limit the width of your image, add the **width** parameter and assign a value ``:width: 400``.

.. tip:: If you need to insert an image multiple times, you can define it like ``.. |Name| image:: /_static/picture.jpg`` and apply it by using ``|Name|`` anywhere.





Add the Comment Function Using Disqus
=======================================
.. note:: Make sure you've got VPN access because Disqus can only be visited via VPN .


Step 1 Install the Library
---------------------------------

In a folder parallel with your Sphinx document directory, create a **requirements-doc.txt** file with the following content:

::

    sphinx
    sphinx_rtd_theme>=0.2.5b2
    -e git://github.com/rmk135/sphinxcontrib-disqus.git#egg=sphinxcontrib-disqus


Run the ``pip install -r requirements-doc.txt`` command to install the library.

.. note:: After the installation, move the **requirements-doc.txt** file into your Sphinx document directory so that it can be sync'ed to GitHub when you commit and push changes.

.. Download the **sphinxcontrib-disqus** library from https://github.com/Robpol86/sphinxcontrib-disqus.git and save it in the same drive with your Sphinx documentation directory.
.. Run the following commands to install the library.
    cd sphinxcontrib-disqus-master
    python setup.py install


Step 2 Configure your Sphinx Documents to Adapt to Disqus
----------------------------------------------------------

In the **conf.py** file, add the following two lines.

::

    extensions = ['sphinxcontrib.disqus']
    disqus_shortname = 'blackmomo'          # ``disqus_shortname`` is defined in your registered Disqus page.


Create a new rst file **comment.rst** with the following script provided by Disqus, and change the variable values.

::

    .. _comment.rst:

    .. raw:: html

     <div id="disqus_thread"></div>
     <script>
     /**
     * RECOMMENDED CONFIGURATION VARIABLES: EDIT AND UNCOMMENT THE SECTION BELOW TO INSERT DYNAMIC VALUES FROM YOUR PLATFORM OR CMS.
       * LEARN WHY DEFINING THESE VARIABLES IS IMPORTANT: https://disqus.com/admin/universalcode/#configuration-variables
         */
         /*
         var disqus_config = function () {
         this.page.url = PAGE_URL; // Replace PAGE_URL with your page's canonical URL variable
         this.page.identifier = PAGE_IDENTIFIER; // Replace PAGE_IDENTIFIER with your page's unique identifier variable
         };
         */
                 var disqus_shortname = 'blackmomo';                // required: replace it with your Disqus shortname 
         (function() { // DON'T EDIT BELOW THIS LINE
         var d = document, s = d.createElement('script');

         s.src = '//blackmomo.disqus.com/embed.js';                 // required: replace it with your Disqus site name

         s.setAttribute('data-timestamp', +new Date());
         (d.head || d.body).appendChild(s);
         })();
         </script>
         <noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript" rel="nofollow">comments powered by Disqus.</a></noscript> 


Add the following line to the topics where the comment function needs to appear.

::

    .. include:: comment.rst


Build your Sphinx documents locally and view the results.

.. note:: For security reasons, Javascript doesn’t load from  ``file://``, only ``http://`` or ``https://``. A simple workaround to view your HTML files through a simple web server after building your HTML files is:

    1. ``cd build/html``
    2. ``python -m http.server 8080``
    3. Browse to http://localhost:8080/


Step 3 Confiure Read the Docs
------------------------------------
In the **Admin > Advanced Settings** page, enter **requirements-doc.txt** in the **Requirements file** field.





*Reference*

- https://robpol86.github.io/sphinxcontrib-disqus/
- https://github.com/Robpol86/sphinxcontrib-disqus/pull/7
- https://zhu45.org/xxks-kkk.github.io.source/kb/sphinx/disqus.html

.. include:: comment.rst
