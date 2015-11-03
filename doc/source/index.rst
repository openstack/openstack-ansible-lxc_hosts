lxc_host role docs
==================

The lxc_host role is used to setup hosts that will be running LXC
within them. The role will configure and build everything needed
for the environment to be successful in deploying LXC containers.

In the example the role is using an optional argument to create an
LXC cached image on the disk. The use of this extra variable will
download an image into place and update it.


Basic Role Example
^^^^^^^^^^^^^^^^^^

.. code-block:: yaml

    - role: "lxc_host"
      lxc_container_caches:
        - url: "{{ repo_pip_default_index | netorigin }}/container_images/rpc-trusty-container.tgz"
          name: "trusty.tgz"
          sha256sum: "56c6a6e132ea7d10be2f3e8104f47136ccf408b30e362133f0dc4a0a9adb4d0c"
          chroot_path: trusty/rootfs-amd64
