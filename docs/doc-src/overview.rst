.. Copyright (c) 2023 OpenHW Group
   SPDX-License-Identifier: Apache-2.0 WITH SHL-2.1

   Level 1
   =======

   Level 2
   -------

   Level 3
   ~~~~~~~

   Level 4
   ^^^^^^^

.. _overview:




CORE-V MCU DevKit Overview
==========================

.. toctree::
    :caption: Table of Contents
    :maxdepth: 1





Short Description
-----------------
The `CORE-V MCU DevKit <https://github.com/openhwgroup/core-v-mcu-devkit>`_ is a turnkey, open-source, development and prototyping platform for the CORE-V MCU System on Chip developed by the members of the `OpenHW Group <https://www.openhwgroup.org>`_. The CORE-V MCU DevKit enables makers of IoT and embedded systems to evaluate the performance of the CORE-V MCU, to interconnect with WiFi and the IoT cloud, and to develop and test software using the `CORE-V-SDK <https://github.com/openhwgroup/core-v-sdk>`_.

License
-------
The CORE-V MCU DevKit is developed under the `Solderpad 2.0 License <https://solderpad.org/licenses/SHL-2.0/>`_


Who Should Read This Document
------------------------------
The following are the intended audience for this document

* Those such as potential users of the CORE-V MCU DevKit who need to understand the overall purpose and function of the DevKit.
* Engineers or others seeking an understanding of the components/BOM of the DevKit.
* Those who need to access the DevKit schematic.
* Those who need a pointer to information and gettig started guide for CORE-V-SDK software. 



Repository
----------
All of the available open-source design artifacts for the CORE-V MCU DevKit can be found in the OpenHW Github repository at https://github.com/openhwgroup/core-v-mcu-devkit

Community Support for CORE-V MCU DevKit
---------------------------------------
Support is available from the development community through Github issues. 
To request support on a particular question or issue, please raise a Github issue at https://github.com/openhwgroup/core-v-mcu-devkit.



OpenSource development at OpenHW Group
--------------------------------------


We encourage people to get involved and contribute to this project.

You can get involved in multiple ways:

- file an issue (either against the DevKit design artifacts or the documentation - we consider erors in both to be bugs!).
- ask a question.
- generate a pull-request.
- propose a derivative project.

As with any activity, we have our ways-of-working that help keep entropy under control.
Specifically, we use git, GitHub and the `Eclipse development process <https://www.eclipse.org/projects/dev_process/>`_.

Git Development Workflow
~~~~~~~~~~~~~~~~~~~~~~~~

Here is a brief description of the development workflow:

1. (Optional) Reach out and open an issue (or grab an open issue) for the
   feature you want to implement. The issue can be a great way of raising the
   attention and is also useful to track the implementation of certain features
   (which can go over multiple pull requests).
2. (Only once) Fork the repository into your own namespace using GitHub (you only need to do
   this once!). `Configure the upstream
   remote <https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/configuring-a-remote-for-a-fork>`_.
3. Synchronize the remote fork and bring it up to date::

   $ git fetch --all
   $ git checkout master
   $ git pull upstream master

4. Clone your forked repository (`xxx` is the username you have forked the
   repository to in step 2.)::

   $ git clone git@github.com:xxxx/core-v-mcu.git

5. Create a new branch for the feature/bug you want to implement/fix. Give the
   branch a meaningful name. You can also prefix it with `feature` or `fix` to
   make the intention more clear. For example if you want to add another CPU
   core you can name your branch `feature/add-new-cpu`. The name of the branch
   isn't super important so you can also pick more concise names.::

   $ git checkout -b feature/add-new-cpu

6. Git will have created this branch and switch to it. Start development.
7. Once you are happy with the contribution (or somewhere in between if you
   think it is worth making a commit), you can add the files to your staging
   area. For example::

   $ git add file/i/ve/touched.txt

8. Commit the changes and add a meaningful commit message::

   $ git commit

9. Push the changes to your GitHub fork.::

   $ git push origin feature/add-new-cpu

10. Open a pull request using the `GitHub
    interface <https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request>`_.
11. Iterate on the pull request interface until all code quality checks are
    passed and the maintainer is happy with the contribution. You can simply
    change files and repeat step 7 - 9. Your pull request will automatically be
    updated and the maintainer notified.
12. The maintainer will merge your changes into the `master` branch. You can now
    finish and delete your branch (if you want). For the next feature go back to
    3.


ECA and Signing Commits
~~~~~~~~~~~~~~~~~~~~~~~

We programmatically enforce signing all your commits and check your email
against the `Eclipse Contributor Agreement <https://www.eclipse.org/legal/ECA.php>`_ database.
Be sure to sign-up with the right email address and add it to either the global or local repository setting.
For example to add it to the local settings execute the following in the local repository::

    $ git config user.email "username@example.com"

Optionally, you can sign your commits by using `git commit -s`.
