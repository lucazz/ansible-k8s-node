Kubernetes Node Role
=========

[![Build Status](https://travis-ci.org/lucazz/ansible-k8s-node.svg?branch=master)](https://travis-ci.org/lucazz/ansible-k8s-node)

Simple Ansible role to installs and configures a Kubernetes node

Requirements
------------

This role only requires Ansible version 2+

Role Variables
--------------

`deployment_controller.src: "template-deployment.yaml.j2"`

`deployment_controller.dest: "/tmp/nginx-test-deployment.yaml"`


Dependencies
------------

This role depends on the following roles:

*   [lucazz.etcd](https://github.com/lucazz/ansible-etcd)
*   [lucazz.calico](https://github.com/lucazz/ansible-calico)
*   [lucazz.k8s-kubelet](https://github.com/lucazz/ansible-k8s-kubelet)
*   [lucazz.k8s-node](https://github.com/lucazz/ansible-k8s-node)

Example Playbook
----------------

Using this roles as as simples as:

    ---
    - hosts: localhost
      remote_user: root
      roles:
        - lucazz.common
        - lucazz.etcd
        - lucazz.calico
        - lucazz.k8s-kubelet
        - lucazz.k8s-node

License
-------

BSD

Author Information
------------------

Lucas do Amaral Saboya Works as Site Reliability Engineer @ [HE:labs](https://www.helabs.com)
