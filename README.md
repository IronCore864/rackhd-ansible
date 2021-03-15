# RackHD 

Everything that is related to RackHD automation.

Unlike the offical ansible playbook/roles, this one is minimum, and it works.

## 1 Inventories

We have 2 inventories for now, which are `local` and `dev`.

The `local` one is 2 VMs using vagrant for local test;

and the `dev` one is for Munich lab, one Lenovo server runs KVM and with 3 VMs inside.

For local ENV, it uses vagrant, if you have other vagrant boxes running, the ssh port might be different, in which case, you need to update the inventory file.

## 2 RackHD Installation

```
ansible-playbook -i inventories/local/ playbooks/rackhd.yml
```

## 3 Infra Server Installation

```
ansible-playbook -i inventories/local/ playbooks/infra.yml
```

This installs NTP server and DNS server.

## 4 Configure All Nodes to use RackHD Server as Time Server

```
ansible-playbook -i inventories/dev playbooks/nodes.yml
```

## 5 Workflow Examples

See [HERE](workflow.md).

