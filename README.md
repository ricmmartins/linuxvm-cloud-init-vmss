# How to use cloud-init on Virtual Machine Scale Set

Going forward on my articles covering the usage of cloud-init, in this last article we will use cloud-init in a Virtual Machine Scale Set. With [Virtual Machine Scale Sets](https://docs.microsoft.com/en-us/azure/virtual-machine-scale-sets/overview) we can have a group of load balanced VMs and the number of VM instances can automatically increase or decrease in response to demand or a defined schedule. Scale sets provide high availability to applications, allowing to centrally manage, configure and update a large number of VMs.

Adding the usage of cloud-init in a VMSS, we can work with an efficient deployment model of applications. In this lab, the idea will be demontrate it using a [simple PHP application](https://github.com/ricmmartins/simple-php-app) being deployed at the VMs under the VMSS at the creation time of each VM. After the deployment, the VMs aren't changed anymore, all artifacts for the applications wil be already deployed within the VMs. This is a concept of Immutable Infrastructure, very well described here [https://medium.com/the-cloud-architect/immutable-infrastructure-21f6613e7a23#](https://medium.com/the-cloud-architect/immutable-infrastructure-21f6613e7a23#) and here [https://www.perylemke.com/posts/infra-imutavel/](https://www.perylemke.com/posts/infra-imutavel/) (in Brazilian-Portuguese)

✔️ Use the Bash environment in [Azure Cloud Shell](https://docs.microsoft.com/en-us/azure/cloud-shell/quickstart).

[![launch-cloud-shell.png)](launch-cloud-shell.png)](http://shell.azure.com/)
