

.. index:: worklog3


===========================
Working with Git
===========================



Commit Changes to Another Branch
===================================
For example, the current branch I'm working on is named **master**, and the other branch is named **stable**.
#. Run ``$ git checkout -b stable`` to switch to the new branch.
#. Run ``$ git commit -m "subject change"`` to commit the change.
#. Run ``$ git push origin stable`` to push the changes to the new branch.

