First of all, if you want everything to be fine, you do definitely need to:
1. Turn off or set to permissive SElinux/apparmor;
2. Turn off or allow required ports in your firewall settings;
3. Make sure you time is synchronized on all of you nodes;
4. Your locale settings are configured properly.

These are simple implementations of different load balancers:
***
1) L4 HAproxy with SSL termination and keepalived;
2) L7 HAproxy with SSL termination and keepalived;
3) Keepalived as a load balancer solo in NAT mode;
4) Ngnix as a load balancer.
***

You may need extra ansible-galaxy collection to work with certificates:
```
ansible-galaxy collection install community.crypto
```
These playbooks have been tested on **Centos7** and **Ubuntu 20.04**.