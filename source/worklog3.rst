

.. index:: worklog3


===========================
Working with Git
===========================



Commit Changes to Another Branch
===================================
For example, the current branch I'm working on is named **master**, and the other branch is named **stable**.

#. Run ``$ git checkout -b stable`` to switch to the new branch.
#. Run ``$ git commit <file> -m "sync with master"`` to commit a single change to your local repo.
#. Run ``$ git push origin stable`` to push the change to the new branch on the Github.

