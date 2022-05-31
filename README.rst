The Host hypervisor(Running KVM/QEMU + Virtual Machine Manager) basically acts like the seed server orchestrating all of the VMs.
Following method of Deploying Openstack using Kolla-Ansible once the Openstack environment is built, 
One can run basic Openstack command and practice.

Since the vNICs are not routable outside the internal network, I had done SSH tunnel to access the individual nodes from your laptop.
For example – Hypervisor management is 10.42.52.17 then create a SSH tunnel with a unique port number to the internal VM IP 192.168.122.100 as follows.
You need to have the SSH key copied –

ssh-keygen
ssh-copy-id username@hostip
ssh -L 10.42.52.17:9001:192.168.122.100:22 openstack@controller01 -N

Another lazy option is to setup GUI on Ubuntu and setup of xrdp but this will limit the number of concurrent sessions I think.
Happy learning !!!
