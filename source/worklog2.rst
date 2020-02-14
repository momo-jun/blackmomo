

.. index:: worklog2


===========================
Working with Read the Docs
===========================



Multi-version
===============
#. Create a new branch for your project on Github.
#. On the Versions tab of RTD, activate the new version (synced from Github).
#. Build the new version.




Multi-language for Localization
================================

Step 1 Create Translatable Files
---------------------------------
Run ``$ sphinx-build -b gettext . _build/gettext`` in the **source/** directory to create **pot** files.


Step 2 Translate Text from Source Language
-------------------------------------------
#. Run ``$ pip install-intl`` to install the **sphinx-intl** tool.
#. Run ``$ sphinx-intl update -p _build/gettext -l ja_JP`` to generate a directory structure like below:

::

	locale
	├── ja_JP
	│   └── LC_MESSAGES
	│       └── index.po

Then open those **.po** files with a text editor and translate the content in the **msgstr** argument.


Step 3 Build the Documentation in Target Language
---------------------------------------------------
Run ``$ sphinx-build -b html -D language=ja_JP . _build/html/ja_JP`` to build the documentation in Japanese.



*Reference*

- https://docs.readthedocs.io/en/stable/guides/manage-translations.html
- https://docs.readthedocs.io/en/stable/localization.html
- https://www.icanlocalize.com/site/tutorials/how-to-translate-with-gettext-po-and-pot-files/
- https://www.drupal.org/node/1814954


.. include:: comment.rst