ceph-ansible
============

Ansible Playbooks for Ceph: a collection of playbooks to get started with
a Ceph cluster and provision them easily.

Make sure you refer to the `getting started guide <http://ceph.com/docs/master/start/quick-start-preflight/>_` before
provisioning a cluster.

``vagrant`` ready
-----------------
All playbooks come with a ``vagrant`` file for local development, so getting
started is even easier. Make sure you have Vagrant versions >= 1.2.0

Getting Started
---------------
There are a couple of requirements to use these playbooks. Because we are also
using Vagrant, make sure you have version ``1.2.0`` at the very least (some
config commands will not work otherwise).

After cloning this repository, create a virtualenv and activate it::

    $ git clone https://github.com/alfredodeza/ceph-ansible.git
    $ cd ceph-ansible
    $ virtualenv .
    $ source bin/activate

The virtualenv will allow you to install the latest version of ansible and not
polute your environment. Install it by running::

    $ pip install ansible

Once that completes, you can run the ``development`` version of this
repository. Change directories to ``development`` and run vagrant::

    $ cd development
    $ vagrant up

The development version will use the ``precise`` release of Ubuntu, download
the VM, install the minimum necessary for Ceph and get the repositories for the
debian packages.

After the vagrant command completes, you are ready to play with Ceph!

Again, you just went through the `getting started guide <http://ceph.com/docs/master/start/quick-start-preflight/>_` , but in an
automated way.

You can now go through the `store cluster quick start <http://ceph.com/docs/master/start/quick-ceph-deploy/>`_ to actually start
using Ceph.
