Getting started
===============

.. contents::
   :local:

.. include:: includes/all.rst


Example inventory
-----------------

To manage Apache on a given host it should be included in the
``debops_service_apache`` Ansible inventory group:

.. code:: ini

   [debops_service_apache]
   hostname

Example playbook
----------------

If you are using this role without DebOps, here's an example Ansible playbook
that uses the ``debops.apache`` role:

.. literalinclude:: playbooks/apache.yml
   :language: yaml

Ansible tags
------------

You can use Ansible ``--tags`` or ``--skip-tags`` parameters to limit what
tasks are performed during Ansible run. This can be used after host is first
configured to speed up playbook execution, when you are sure that most of the
configuration has not been changed.

Available role tags:

``role::apache``
  Main role tag, should be used in the playbook to execute all of the role
  tasks as well as role dependencies.

``role::apache:pkgs``
  Tasks related to system package management like installing or removing
  packages.

``role::apache:modules``
  Tasks related to Apache modules.

``role::apache:vhosts``
  Tasks related to Apache virtual hosts.
