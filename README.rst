OpenStack-Ansible LXC hosts
###########################

Ansible role that configures a host for running LXC containers.

Default Variables
=================

.. literalinclude:: ../../defaults/main.yml
   :language: yaml
   :start-after: under the License.

Required Variables
==================

None

Example Playbook
================

.. code-block:: yaml

    - name: Basic lxc host setup
      hosts: "hosts"
      user: root
      roles:
        - { role: "lxc_hosts" }

