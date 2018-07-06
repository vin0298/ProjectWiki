# Vagrant

Vagrant is a tool for building and managing virtual machine environments in a single workflow with focus on automation.

From [Vagrant documentation](https://www.vagrantup.com/intro/index.html)

## Quickly setup a vagrant virtual machine
Type on the terminal, change the "hashicorp/precise64" with the box you need. All boxes can be found [here](https://vagrantcloud.com/boxes/search)
```
vagrant box add hashicorp/precise64
```
This will create a VM called "default". To customize VM configuration, you can edit the vagrantfile on the current directory.<br>
Tutorial on configuring the vagrantfile can be found [here](https://www.youtube.com/watch?v=pofWJAHynfU&index=6&list=PLMWwct3_kb-358XZdnN66zb3HaU97DSQ0)<br>
Tutorial on setting up multiple VM can be found [here](https://www.youtube.com/watch?v=RSslFGH1Vjw)

To create and start VM, type :
```
vagrant up <VM name>
```
If you don't specify the VM name, it will boot all VM you have

<br>

To shut down the VM, type :
```
vagrant halt <VM name>
```
If you don't specify the VM name, it will shut down all VM you have

<br>

To ssh to the VM, type :
```
vagrant ssh <VM name>
```

<br>

To list all VM and its statuses, type :
```
vagrant ssh <VM name>
```
