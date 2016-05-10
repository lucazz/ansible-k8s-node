Kubernetes Node Role
=========

[![Build Status](https://travis-ci.org/lucazz/ansible-k8s-master.svg?branch=master)](https://travis-ci.org/lucazz/ansible-k8s-master)

Simple Ansible role to installs and configures a Kubernetes Master

Requirements
------------

This role only requires Ansible version 1.9+

Role Variables
--------------

`containers.cidr: "192.168.0.0/16"`

`etcd.address: "{{ ansible_default_ipv4.address }}"`

`etcd.port: 2379`

`k8s.master_address: "{{ ansible_default_ipv4.address }}"`

`k8s.cidr: "10.100.0.0/16"`

`k8s.port: 8080`

`k8s.bind_mask: "0.0.0.0"`

Dependencies
------------

This role depends on the following roles:

*   [lucazz.etcd](https://github.com/lucazz/ansible-etcd)
*   [lucazz.calico](https://github.com/lucazz/ansible-calico)
*   [lucazz.kubelet](#)

Example Playbook
----------------

Using this roles as as simples as:

    - hosts: servers
      roles:
        - lucazz.common
        - lucazz.etcd
        - lucazz.calico
        - lucazz.k8s-kubelet
        - lucazz.k8s.master

License
-------

BSD

Author Information
------------------

Lucas do Amaral Saboya Works as Site Reliability Engineer @ [HE:labs](https://www.helabs.com)
