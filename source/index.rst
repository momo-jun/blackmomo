.. Jun documentation master file, created by
   sphinx-quickstart on Mon Feb  3 17:19:00 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to Jun's documentation!
===============================


Treating documentation as code is becoming a major theme in the software industry.

This page is only used to document the information I gathered and the process I went through when I did pratices on Git, ReadtheDocs, and Sphinx.


Background:
-----------
* Sphinx provides a documentation generator that is best-in-class for software docs. Sphinx documents are written in the reStructuredText markup language.
reStructuredText is a powerful language primarily because the syntax can be extended.
* Read the Docs is a hosting platform for Sphinx-generated documentation. It takes the power of Sphinx and adds version control, full-text search, and other useful features. It pulls down code and doc files from Git, Mercurial, or Subversion, then builds and hosts your documentation.
*GitHub is a code hosting platform for version control and collaboration.

Preparations:
--------------
* Run python-3.7.5-amd64.exe to install Python 3.7.5
* Run pip install -U Sphinx in the command prompt to install Sphinx
* Run Sublime Text Build 3211 x64 Setup.exe to install Sublime
* Run Git-2.25.0-64-bit.exe to install Git
* Create an account for Read the Docs and Github


Steps:
--------------
# Run $ sphinx-quickstart in the command prompt to build a directory for Sphinx output.
# Create a Repo in Github.
# Connect the local directory and files to your Github Repo by running the following commands in Git Bash.

``$ git config --global user.email "registered email address" //Verify Identity
$ git config --global user.name "registered user ID"  //Verify Identity
$ git remote add origin https://github.com/"UserID"/"RepoID".git  //Connect to Github Repo
$ git pull origin master --allow-unrelated-histories
$ git commit -m "description"  //Commit files with a description
$ git push -u origin master  //Push updates``

# Enrich the master file index.rst and other source files by using Sublime.
Syntax: https://www.sphinx-doc.org/en/master/usage/restructuredtext/index.html
# Link your GitHub repo to your Read the Docs account.
# Build and View in Read the Docs.




.. toctree::
   :maxdepth: 2
   :caption: Contents:

   menu
   worklog
   plan



Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
