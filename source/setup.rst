
====================================
Heading to Sphinx and Read the Docs
====================================


.. note:: This page is only used to document the information I gathered and the process I went through when I did pratices on Git, ReadtheDocs, and Sphinx.


Background
-----------
Treating documentation as code is becoming a major theme in the software industry.

The following advanced tools and platforms are widely used by both developers and technical writers.

* Sphinx provides a documentation generator that is best-in-class for software docs. Sphinx documents are written in the reStructuredText markup language. reStructuredText is a powerful language primarily because the syntax can be extended.

* Read the Docs is a hosting platform for Sphinx-generated documentation. It takes the power of Sphinx and adds version control, full-text search, and other useful features. It pulls down code and doc files from Git, Mercurial, or Subversion, then builds and hosts your documentation.

* GitHub is a code hosting platform for version control and collaboration.


Preparations
--------------
* Run **python-3.7.5-amd64.exe** to install Python 3.7.5
* Run ``pip install -U Sphinx`` in the command prompt to install Sphinx
* Run **Sublime Text Build 3211 x64 Setup.exe** to install Sublime
* Run **Git-2.25.0-64-bit.exe** to install Git
* Create an account in Read the Docs and Github


Steps
-------------------
#. Run ``$ sphinx-quickstart`` in the command prompt to build a directory for Sphinx output.
#. Enrich the master file index.rst and other source files by using Sublime. 

	.. tip:: To learn more Sphinx syntax, refer to https://www.sphinx-doc.org/en/master/usage/restructuredtext/index.html.

#. Create an open-source repo in Github.
#. Commit the local directory and files to your Github Repo by running the following commands in Git Bash.

	- Verify Identity: ``$ git config --global user.email "registered email address"``
	- Verify Identity: ``$ git config --global user.name "registered user ID"``
	- Connect to Github Repo: ``$ git remote add origin https://github.com/"UserID"/"RepoID".git``
	- Create a Pull Request and Merge: ``$ git pull origin master --allow-unrelated-histories``
	- Add all files: ``$ git add *``
	- Commit all files you added: ``$ git commit -m "description"``
	- Push and merge updates: ``$ git push -u origin master``

#. Link your GitHub repo to your Read the Docs account.
#. Build and View in Read the Docs.


