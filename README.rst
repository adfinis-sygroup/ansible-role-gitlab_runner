==================
ROLE GITLAB_RUNNER
==================

.. image:: https://img.shields.io/github/license/adfinis-sygroup/ansible-role-gitlab_runner.svg?style=flat-square
  :target: https://github.com/adfinis-sygroup/ansible-role-gitlab_runner/blob/master/LICENSE

.. image:: https://img.shields.io/travis/adfinis-sygroup/ansible-role-gitlab_runner.svg?style=flat-square
  :target: https://travis-ci.org/adfinis-sygroup/ansible-role-gitlab_runner

.. image:: https://img.shields.io/badge/galaxy-adfinis--sygroup.gitlab_runner-660198.svg?style=flat-square
  :target: https://galaxy.ansible.com/adfinis-sygroup/gitlab_runner

This role is used to install a new gitlab runner and register it.


Role Variables
===============

The following variables are available:

.. code-block:: yaml

  # The URL of the GitLab to register to
  gitlab_runner_ci_url: 'https://git.example.com'

  # The token needed for registering the runner
  # https://git.adfinis-sygroup.ch/admin/runners
  gitlab_runner_ci_token: 'my_ci_token'

  # The docker images used as default image
  gitlab_runner_docker_image: 'docker:stable'

  # Run the container in priviledged mode or not
  gitlab_runner_docker_privileged: True

  # The default package list
  gitlab_runner_package_list:
    - ca-certificates
    - gitlab-runner


Example Playbook
=================


.. code-block:: yaml

  - hosts: gitlab-runners
    vars:
      gitlab_runner_ci_url: 'https://git.example.com'
      gitlab_runner_ci_token: 'thisismytoken'
    roles:
       - { role: adfinis-sygroup.gitlab_runner }


License
========

`GPL-3.0 <https://github.com/adfinis-sygroup/ansible-role-gitlab_runner/blob/master/LICENSE>`_


Author Information
===================

gitlab_runner role was written by:

* Adfinis SyGroup AG | `Website <https://www.adfinis-sygroup.ch/>`_ | `Twitter <https://twitter.com/adfinissygroup>`_ | `GitHub <https://github.com/adfinis-sygroup>`_

