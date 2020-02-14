

.. index:: worklog3


===========================
Working with Git
===========================



Commit Changes to A New Branch
===================================
For example, the current branch I'm working on is named **master**, and the other branch is named **stable**.

#. Run ``$ git checkout -b stable`` to switch to the new branch.
#. Edit files and save.
#. Run ``$ git commit <file> -m "sync with master"`` to commit a single change to your local repo.
#. Run ``$ git push origin stable`` to push the change to the new branch on the Github.


Merge Changes into the Master Branch
=========================================
The current branch I'm working on is named **stable**.

#. Run ``$ git checkout master`` to switch to the master branch.
#. Run ``$ git merge stable``.

.. include:: comment.rst
