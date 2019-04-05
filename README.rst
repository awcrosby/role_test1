Installing
==========

.. installing-docs-inclusion-marker-do-not-remove

Using Pip
---------

.. code-block:: bash

    pip install ansible-lint

.. _installing_from_source:

From Source
-----------

.. code-block:: bash

    pip install git+https://github.com/ansible/ansible-lint.git

.. installing-docs-inclusion-marker-end-do-not-remove

Usage
=====

.. usage-docs-inclusion-marker-do-not-remove

Command Line Options
--------------------

The following is the output from ``ansible-lint --help``, providing an overview of the basic command line options:

.. code-block:: bash

    Usage: ansible-lint playbook.yml|roledirectory ...

    Options:
      --version             show program's version number and exit
      -h, --help            show this help message and exit
      -L                    list all the rules
      -q                    quieter, although not silent output
      -p                    parseable output in the format of pep8
      -r RULESDIR           specify one or more rules directories using one or
                            more -r arguments. Any -r flags override the default
                            rules in ['/path/to/ansible-
                            lint/lib/ansiblelint/rules'], unless -R is also used.
      -R                    Use default rules ['/path/to/ansible-
                            lint/lib/ansiblelint/rules'] in addition to any extra
                            rules directories specified with -r. There is no need
                            to specify this if no -r flags are used
      -t TAGS               only check rules whose id/tags match these values
      -T                    list all the tags
      -x SKIP_LIST          only check rules whose id/tags do not match these
                            values
      --exclude=EXCLUDE_PATHS
                            path to directories or files to skip. This option is
                            repeatable.
      --force-color         Try force colored output (relying on ansible's code)
      --nocolor             disable colored output
      -c /path/to/file      Specify configuration file to use.  Defaults to
                              ".ansible-lint"



Linting Playbooks and Roles
---------------------------

It's important to note that ``ansible-lint`` accepts a list of Ansible playbook files or a list of role directories. Starting from a directory that contains the following, the playbook file, ``playbook.yml``, or one of the role subdirectories, such as ``geerlingguy.apache``, can be passed: