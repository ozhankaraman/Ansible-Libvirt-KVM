# Ansible Libvirt KVM
Repository to create Ubuntu 1604/1804 and Centos 7 Virtual Machines for ZebraStack and Zebra Bulut 

To deploy a vm named vx2, first we need to create vx2.yml file under variables file and then execute the deploy_vm.yml playbook like below:

ansible-playbook deploy_vm.yml -e hostname=vx2

Notes:
* If there are currently defined vm's with same name over the hypervisor then that vm will be redeployed again
* Qcow2 images are automatically build by HashiCorp's Packer.IO tool
*

apt-get install -y qemu-kvm libvirt-bin bridge-utils libguestfs-tools python-libvirt
