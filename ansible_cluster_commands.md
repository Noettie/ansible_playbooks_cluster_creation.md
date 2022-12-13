Last login: Sun Dec 11 22:35:44 2022 from 70.115.102.190
ubuntu@Ansible-server:~$ history
    1  clear
    2  sudo vi /etc/hostname
    3  sudo init 6
    4  clear
    5  sudo apt-get update
    6  sudo apt update
    7  sudo apt upgrade
    8  sudo apt install software-properties-common
    9  sudo add-apt-repository --yes --update ppa:ansible/ansible
   10  sudo apt install ansible
   11  ansible --version
   12  clear
   13  mkdir kube-cluster
   14  cd kube-cluster/\
   15  ls
   16  vi hosts
   17  vi initial.yml
   18  ansible-playbook -i hosts ~/kube-cluster/initial.yml
   19  clear
   20  ssh key-gen
   21  ssh-keygen
   22  ssh-copy-id ubuntu@172.31.11.58
   23  ssh-copy-id ubuntu@172.31.13.26
   24  ssh-copy-id ubuntu@172.31.13.122
   25  ansible-playbook -i hosts ~/kube-cluster/initial.yml
   26  ls
   27  clear
   28  vi kube-dependencies.yml
   29  ls
   30  vi kube-dependencies.yml
   31  ls
   32  vi hosts
   33  sudo ansible -m ping all
   34  vi hosts
   35  vi /etc/hosts
   36  sudo vi /etc/hosts
   37  sudo ansible -m ping all
   38  sudo vi /etc/hosts
   39  sudo ansible -m ping all
   40  sudo vi /etc/hosts
   41  sudo /etc/ansible/hosts
   42  sudo vim /etc/ansible/hosts
   43  sudo ansible -m ping all
   44  clear
   45  chmod +w  ~/.ssh/known_hosts
   46  sudo ansible -m ping all
   47  sudo vi /etc/ssh/ssh_config
   48  sudo ansible -m ping all
   49  clear
   50  ssh-keygen -f ~/.ssh/id_ecdsa -t ecdsa -b 521
   51  ssh-copy-id -i ~/.ssh/id_ecdsa ubuntu@172.31.11.58
   52  ssh ubuntu@172.31.11.58
   53  ssh-copy-id -i ~/.ssh/id_ecdsa ubuntu@172.31.13.26
   54  sss ubuntu@172.31.13.26
   55  ssh ubuntu@172.31.13.26
   56  clear
   57  ssh-copy-id -i ~/.ssh/id_ecdsa ubuntu@172.31.13.122
   58  ssh ubuntu@172.31.13.122
   59  clear
   60  sudo ansible -m ping all
   61  ssh-copy-id localhost
   62  sudo ssh-copy-id localhost
   63  ssh-copy-id localhost
   64  ssh-copy-id -i ~/.ssh/id_ecdsa ubuntu@localhost
   65  sudo ansible -m ping all
   66  clear
   67  sudo /etc/ansible/hosts
   68  sudo vi /etc/ansible/hosts
   69  sudo ansible -m ping all
   70  ansible all -m ping --ask-pass --ask-sudo-pass
   71  ansible all -m ping --ask-pass --ask-sudo-pass -u
   72  clear
   73  ansible all -m ping --ask-pass
   74  ansible all -m ping
   75  clear
   76  ansible all -m ping
   77  vi initial.yml
   78  ls
   79  vi initial.yml
   80  vi dependencies.yml
   81  clear
   82  ansible-playbook -i hosts ~/kube-cluster/kube-dependencies.yml
   83  sudo vi /etc/ansible/hosts
   84  ansible all -m ping --ask-pass
   85  sudo vi /etc/ansible/hosts
   86  ansible all -m ping --ask-pass
   87  sudo vi /etc/ansible/hosts
   88  ansible all -m ping --ask-pass
   89  ls
   90  vi kube-dependencies.yml
   91  ansible all -m ping --ask-pass
   92  ansible-playbook -i hosts ~/kube-cluster/kube-dependencies.yml
   93  sudo vi ~/.ssh/known_hosts
   94  sudo vi ~/.ssh/config
   95  ls -ls
   96  ls -la
   97  cd .
   98  ls
   99  clear
  100  cd /
  101  sudo su
  102  history

ubuntu@Ansible-server:~$ ansible-playbook -i hosts ~/kube-cluster/initial.yml

PLAY [all] *************************************************************************************************************************************************

TASK [Gathering Facts] *************************************************************************************************************************************
fatal: [worker3]: UNREACHABLE! => {"changed": false, "msg": "Failed to connect to the host via ssh: Warning: Permanently added '3.222.245.224' (ED25519) to  of known hosts.\r\nubuntu@3.222.245.224: Permission denied (publickey).", "unreachable": true}
ok: [worker2]
ok: [worker1]
ok: [control1]

TASK [create the 'ubuntu' user] ****************************************************************************************************************************
[WARNING]: 'append' is set, but no 'groups' are specified. Use 'groups' for appending new groups.This will change to an error in Ansible 2.14.
ok: [worker2]
ok: [worker1]
ok: [control1]

TASK [allow 'ubuntu' to have passwordless sudo] ************************************************************************************************************
ok: [worker1]
ok: [worker2]
ok: [control1]

TASK [set up authorized keys for the ubuntu user] **********************************************************************************************************
ok: [worker2] => (item=ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDFGvJddbc0Q4/7ORW42fEOgbNPQFLTtvol6LGYRQQs7cEVm3O//peyiAXmGR3/eid2qB4jLN5hdAu1HUbmj0eM8gmAYSJhfKxmnQ0N6JX1lMBJY9c8jolT2CFPRITuaBwtLknd6ET4WG1glC3+s+6OwC7536g4xp9tuE+tGlxiJQrRCHRq4hvWH8IvQmZZKX1mcA668drffni8uMi8EgNlvwcVfVKKjwvWpP2wq0Mi6Kt98KSj3UFtkzgntArI6VH1ipqPw1VlwABjeJmUgDo5jzpGB5xLW+C9ymSMFx3o/JafSkQiPOGCT3nl/YW5dEhtQKA64W970CNONw1CrGHq7QKCgwN0sSW5pag/MvErefCN37OQiJ5Fb+oF+8FYc7eNeeDxs+reC/NMXfK7hHcAItVNi3pvh7/cYEqhAueU3TcQOemwSSHDA3fh85FTCKTcFtIJI2SxKzSwPA+Psbm3fKvrijMIV3GieNKsTck= ubuntu@Ansible-server)
ok: [worker1] => (item=ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDFGvJddbc0Q4/7ORW42fEOgbNPQFLTtvol6LGYRQQs7cEVm3O//peyiAXmGR3/eid2qB4jLN5hdAu1HUbmj0eM8gmAYSJhfKxmnQ0N6JX1lMBJY9c8jolT2CFPRITuaBwtLknd6ET4WG1glC3+s+6OwC7536g4xp9tuE+tGlxiJQrRCHRq4hvWH8IvQmZZKX1mcA668drffni8uMi8EgNlvwcVfVKKjwvWpP2wq0Mi6Kt98KSj3UFtkzgntArI6VH1ipqPw1VlwABjeJmUgDo5jzpGB5xLW+C9ymSMFx3o/JafSkQiPOGCT3nl/YW5dEhtQKA64W970CNONw1CrGHq7QKCgwN0sSW5pag/MvErefCN37OQiJ5Fb+oF+8FYc7eNeeDxs+reC/NMXfK7hHcAItVNi3pvh7/cYEqhAueU3TcQOemwSSHDA3fh85FTCKTcFtIJI2SxKzSwPA+Psbm3fKvrijMIV3GieNKsTck= ubuntu@Ansible-server)
ok: [control1] => (item=ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDFGvJddbc0Q4/7ORW42fEOgbNPQFLTtvol6LGYRQQs7cEVm3O//peyiAXmGR3/eid2qB4jLN5hdAu1HUbmj0eM8gmAYSJhYKxmnQ0N6JX1lMBJY9c8jolT2CFPRITuaBwtLknd6ET4WG1glC3+s+6OwC7536g4xp9tuE+tGlxiJQrRCHRq4hvWH8IvQmZZKX1mcA668drffni8uMi8EgNlvwcVfVKKjwvWpP2wq0Mi6Kt98KSj3UFtkzgnJArI6VH1ipqPw1VlwABjeJmUgDo5jzpGB5xLW+C9ymSMFx3o/JafSkQiPOGCT3nl/YW5dEhtQKA64W970CNONw1CrGHq7QKCgwN0sSW5pag/MvErefCN37OQiJ5Fb+oF+8FYc7eNeeDxs+reC/NMXfK7hHcActVNi3pvh7/cYEqhAueU3TcQOemwSSHDA3fh85FTCKTcFtIJI2SxKzSwPA+Psbm3fKvrijMIV3GieNKsTck= ubuntu@Ansible-server)

PLAY RECAP *************************************************************************************************************************************************
control1                   : ok=4    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
worker1                    : ok=4    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
worker2                    : ok=4    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
worker3                    : ok=0    changed=0    unreachable=1    failed=0    skipped=0    rescued=0    ignored=0

ubuntu@Ansible-server:~$ ls
control-plane.yml  hosts  kube-cluster  kube-dependencies.yml  workers.yml
ubuntu@Ansible-server:~$ vi hosts
ubuntu@Ansible-server:~$ sudo vi /etc/ansible/ansible.cfg
ubuntu@Ansible-server:~$ vi hosts
ubuntu@Ansible-server:~$ ansible-playbook -i hosts ~/kube-cluster/initial.yml

PLAY [all] *************************************************************************************************************************************************

TASK [Gathering Facts] *************************************************************************************************************************************
ok: [worker1]
ok: [worker2]
ok: [control1]

TASK [create the 'ubuntu' user] ****************************************************************************************************************************
[WARNING]: 'append' is set, but no 'groups' are specified. Use 'groups' for appending new groups.This will change to an error in Ansible 2.14.
ok: [worker2]
ok: [control1]
ok: [worker1]

TASK [allow 'ubuntu' to have passwordless sudo] ************************************************************************************************************
ok: [worker2]
ok: [control1]
ok: [worker1]

TASK [set up authorized keys for the ubuntu user] **********************************************************************************************************
ok: [worker2] => (item=ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDFGvJddbc0Q4/7ORW42fEOgbNPQFLTtvol6LGYRQQs7cEVm3O//peyiAXmGR3/eid2qB4jLN5hdAu1HUbmj0eM8gmAYSJhfKxmnQ0N6JX1lMBJY9c8jolT2CFPRITuaBwtLknd6ET4WG1glC3+s+6OwC7536g4xp9tuE+tGlxiJQrRCHRq4hvWH8IvQmZZKX1mcA668drffni8uMi8EgNlvwcVfVKKjwvWpP2wq0Mi6Kt98KSj3UFtkzgntArI6VH1ipqPw1VlwABjeJmUgDo5jzpGB5xLW+C9ymSMFx3o/JafSkQiPOGCT3nl/YW5dEhtQKA64W970CNONw1CrGHq7QKCgwN0sSW5pag/MvErefCN37OQiJ5Fb+oF+8FYc7eNeeDxs+reC/NMXfK7hHcAItVNi3pvh7/cYEqhAueU3TcQOemwSSHDA3fh85FTCKTcFtIJI2SxKzSwPA+Psbm3fKvrijMIV3GieNKsTck= ubuntu@Ansible-server)
ok: [worker1] => (item=ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDFGvJddbc0Q4/7ORW42fEOgbNPQFLTtvol6LGYRQQs7cEVm3O//peyiAXmGR3/eid2qB4jLN5hdAu1HUbmj0eM8gmAYSJhfKxmnQ0N6JX1lMBJY9c8jolT2CFPRITuaBwtLknd6ET4WG1glC3+s+6OwC7536g4xp9tuE+tGlxiJQrRCHRq4hvWH8IvQmZZKX1mcA668drffni8uMi8EgNlvwcVfVKKjwvWpP2wq0Mi6Kt98KSj3UFtkzgntArI6VH1ipqPw1VlwABjeJmUgDo5jzpGB5xLW+C9ymSMFx3o/JafSkQiPOGCT3nl/YW5dEhtQKA64W970CNONw1CrGHq7QKCgwN0sSW5pag/MvErefCN37OQiJ5Fb+oF+8FYc7eNeeDxs+reC/NMXfK7hHcAItVNi3pvh7/cYEqhAueU3TcQOemwSSHDA3fh85FTCKTcFtIJI2SxKzSwPA+Psbm3fKvrijMIV3GieNKsTck= ubuntu@Ansible-server)
ok: [control1] => (item=ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDFGvJddbc0Q4/7ORW42fEOgbNPQFLTtvol6LGYRQQs7cEVm3O//peyiAXmGR3/eid2qB4jLN5hdAu1HUbmj0eM8gmAYSJhYKxmnQ0N6JX1lMBJY9c8jolT2CFPRITuaBwtLknd6ET4WG1glC3+s+6OwC7536g4xp9tuE+tGlxiJQrRCHRq4hvWH8IvQmZZKX1mcA668drffni8uMi8EgNlvwcVfVKKjwvWpP2wq0Mi6Kt98KSj3UFtkzgnJArI6VH1ipqPw1VlwABjeJmUgDo5jzpGB5xLW+C9ymSMFx3o/JafSkQiPOGCT3nl/YW5dEhtQKA64W970CNONw1CrGHq7QKCgwN0sSW5pag/MvErefCN37OQiJ5Fb+oF+8FYc7eNeeDxs+reC/NMXfK7hHcActVNi3pvh7/cYEqhAueU3TcQOemwSSHDA3fh85FTCKTcFtIJI2SxKzSwPA+Psbm3fKvrijMIV3GieNKsTck= ubuntu@Ansible-server)

PLAY RECAP *************************************************************************************************************************************************
control1                   : ok=4    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
worker1                    : ok=4    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
worker2                    : ok=4    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0

ubuntu@Ansible-server:~$ ansible-playbook -i hosts ~/kube-cluster/kube-dependencies.yml

PLAY [all] *************************************************************************************************************************************************

TASK [Gathering Facts] *************************************************************************************************************************************
ok: [worker2]
ok: [worker1]
ok: [control1]

TASK [create Docker config directory] **********************************************************************************************************************
ok: [worker2]
ok: [worker1]
ok: [control1]

TASK [changing Docker to systemd driver] *******************************************************************************************************************
ok: [worker1]
ok: [worker2]
ok: [control1]

TASK [install Docker] **************************************************************************************************************************************
ok: [worker2]
ok: [worker1]
ok: [control1]

TASK [install APT Transport HTTPS] *************************************************************************************************************************
ok: [worker2]
ok: [worker1]
ok: [control1]

TASK [add Kubernetes apt-key] ******************************************************************************************************************************
ok: [worker1]
ok: [worker2]
ok: [control1]

TASK [add Kubernetes' APT repository] **********************************************************************************************************************
ok: [worker2]
ok: [worker1]
ok: [control1]

TASK [install kubelet] *************************************************************************************************************************************
ok: [worker1]
ok: [worker2]
ok: [control1]

TASK [install kubeadm] *************************************************************************************************************************************
ok: [worker1]
ok: [worker2]
ok: [control1]

PLAY [control_plane] ***************************************************************************************************************************************

TASK [Gathering Facts] *************************************************************************************************************************************
ok: [control1]

TASK [install kubectl] *************************************************************************************************************************************
ok: [control1]

PLAY RECAP *************************************************************************************************************************************************
control1                   : ok=11   changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
worker1                    : ok=9    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
worker2                    : ok=9    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0

ubuntu@Ansible-server:~$ ansible-playbook -i hosts ~/kube-cluster/workers.yml

PLAY [control_plane] ***************************************************************************************************************************************

TASK [get join command] ************************************************************************************************************************************
changed: [control1]

TASK [set join command] ************************************************************************************************************************************
ok: [control1]

PLAY [workers] *********************************************************************************************************************************************

TASK [Gathering Facts] *************************************************************************************************************************************
ok: [worker1]
ok: [worker2]

TASK [join cluster] ****************************************************************************************************************************************
ok: [worker1]
ok: [worker2]

PLAY RECAP *************************************************************************************************************************************************
control1                   : ok=2    changed=1    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
worker1                    : ok=2    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
worker2                    : ok=2    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0

ubuntu@Ansible-server:~$ ansible-playbook -i hosts ~/kube-cluster/control-plane.yml

PLAY [control_plane] ***************************************************************************************************************************************

TASK [Gathering Facts] *************************************************************************************************************************************
ok: [control1]

TASK [initialize the cluster] ******************************************************************************************************************************
ok: [control1]

TASK [create .kube directory] ******************************************************************************************************************************
ok: [control1]

TASK [copy admin.conf to user's kube config] ***************************************************************************************************************
ok: [control1]

TASK [install Pod network] *********************************************************************************************************************************
ok: [control1]

PLAY RECAP *************************************************************************************************************************************************
control1                   : ok=5    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0

ubuntu@Ansible-server:~$ ssh ubuntu@3.227.16.245
Warning: Permanently added '3.227.16.245' (ED25519) to the list of known hosts.
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 5.15.0-1026-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

  System information as of Mon Dec 12 08:34:47 UTC 2022

  System load:  0.28              Users logged in:          1
  Usage of /:   57.6% of 7.57GB   IPv4 address for cni0:    10.244.0.1
  Memory usage: 27%               IPv4 address for docker0: 172.17.0.1
  Swap usage:   0%                IPv4 address for eth0:    172.31.11.58
  Processes:    175               IPv4 address for tunl0:   10.244.27.64

 * Ubuntu Pro delivers the most comprehensive open source security and
   compliance features.

   https://ubuntu.com/aws/pro

4 updates can be applied immediately.
To see these additional updates run: apt list --upgradable

New release '22.04.1 LTS' available.
Run 'do-release-upgrade' to upgrade to it.


Last login: Mon Dec 12 08:34:15 2022 from 3.95.61.153
ubuntu@Control-Node:~$ kubectl get nodes
NAME           STATUS   ROLES                  AGE     VERSION
control-node   Ready    control-plane,master   4h18m   v1.22.4
ubuntu@Control-Node:~$
Network error: Software caused connection abort

────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────

Session stopped
    - Press <return> to exit tab
    - Press R to restart session
    - Press S to save terminal output to file
Authenticating with public key "Imported-Openssh-Key"
    ┌──────────────────────────────────────────────────────────────────────┐
    │                 • MobaXterm Personal Edition v22.2 •                 │
    │               (SSH client, X server and network tools)               │
    │                                                                      │
    │ ⮞ SSH session to ubuntu@3.95.61.153                                  │
    │   • Direct SSH      :  ✓                                             │
    │   • SSH compression :  ✓                                             │
    │   • SSH-browser     :  ✓                                             │
    │   • X11-forwarding  :  ✓  (remote display is forwarded through SSH)  │
    │                                                                      │
    │ ⮞ For more info, ctrl+click on help or visit our website.            │
    └──────────────────────────────────────────────────────────────────────┘

Welcome to Ubuntu 22.04.1 LTS (GNU/Linux 5.15.0-1026-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

  System information as of Sun Dec 11 22:31:29 UTC 2022

  System load:  0.1142578125      Processes:             103
  Usage of /:   19.8% of 7.57GB   Users logged in:       0
  Memory usage: 21%               IPv4 address for eth0: 172.31.26.37
  Swap usage:   0%

 * Ubuntu Pro delivers the most comprehensive open source security and
   compliance features.

   https://ubuntu.com/aws/pro

0 updates can be applied immediately.


Last login: Sun Dec 11 22:35:44 2022 from 70.115.102.190
ubuntu@Ansible-server:~$ history
    1  clear
    2  sudo vi /etc/hostname
    3  sudo init 6
    4  clear
    5  sudo apt-get update
    6  sudo apt update
    7  sudo apt upgrade
    8  sudo apt install software-properties-common
    9  sudo add-apt-repository --yes --update ppa:ansible/ansible
   10  sudo apt install ansible
   11  ansible --version
   12  clear
   13  mkdir kube-cluster
   14  cd kube-cluster/\
   15  ls
   16  vi hosts
   17  vi initial.yml
   18  ansible-playbook -i hosts ~/kube-cluster/initial.yml
   19  clear
   20  ssh key-gen
   21  ssh-keygen
   22  ssh-copy-id ubuntu@172.31.11.58
   23  ssh-copy-id ubuntu@172.31.13.26
   24  ssh-copy-id ubuntu@172.31.13.122
   25  ansible-playbook -i hosts ~/kube-cluster/initial.yml
   26  ls
   27  clear
   28  vi kube-dependencies.yml
   29  ls
   30  vi kube-dependencies.yml
   31  ls
   32  vi hosts
   33  sudo ansible -m ping all
   34  vi hosts
   35  vi /etc/hosts
   36  sudo vi /etc/hosts
   37  sudo ansible -m ping all
   38  sudo vi /etc/hosts
   39  sudo ansible -m ping all
   40  sudo vi /etc/hosts
   41  sudo /etc/ansible/hosts
   42  sudo vim /etc/ansible/hosts
   43  sudo ansible -m ping all
   44  clear
   45  chmod +w  ~/.ssh/known_hosts
   46  sudo ansible -m ping all
   47  sudo vi /etc/ssh/ssh_config
   48  sudo ansible -m ping all
   49  clear
   50  ssh-keygen -f ~/.ssh/id_ecdsa -t ecdsa -b 521
   51  ssh-copy-id -i ~/.ssh/id_ecdsa ubuntu@172.31.11.58
   52  ssh ubuntu@172.31.11.58
   53  ssh-copy-id -i ~/.ssh/id_ecdsa ubuntu@172.31.13.26
   54  sss ubuntu@172.31.13.26
   55  ssh ubuntu@172.31.13.26
   56  clear
   57  ssh-copy-id -i ~/.ssh/id_ecdsa ubuntu@172.31.13.122
   58  ssh ubuntu@172.31.13.122
   59  clear
   60  sudo ansible -m ping all
   61  ssh-copy-id localhost
   62  sudo ssh-copy-id localhost
   63  ssh-copy-id localhost
   64  ssh-copy-id -i ~/.ssh/id_ecdsa ubuntu@localhost
   65  sudo ansible -m ping all
   66  clear
   67  sudo /etc/ansible/hosts
   68  sudo vi /etc/ansible/hosts
   69  sudo ansible -m ping all
   70  ansible all -m ping --ask-pass --ask-sudo-pass
   71  ansible all -m ping --ask-pass --ask-sudo-pass -u
   72  clear
   73  ansible all -m ping --ask-pass
   74  ansible all -m ping
   75  clear
   76  ansible all -m ping
   77  vi initial.yml
   78  ls
   79  vi initial.yml
   80  vi dependencies.yml
   81  clear
   82  ansible-playbook -i hosts ~/kube-cluster/kube-dependencies.yml
   83  sudo vi /etc/ansible/hosts
   84  ansible all -m ping --ask-pass
   85  sudo vi /etc/ansible/hosts
   86  ansible all -m ping --ask-pass
   87  sudo vi /etc/ansible/hosts
   88  ansible all -m ping --ask-pass
   89  ls
   90  vi kube-dependencies.yml
   91  ansible all -m ping --ask-pass
   92  ansible-playbook -i hosts ~/kube-cluster/kube-dependencies.yml
   93  sudo vi ~/.ssh/known_hosts
   94  sudo vi ~/.ssh/config
   95  ls -ls
   96  ls -la
   97  cd .
   98  ls
   99  clear
  100  cd /
  101  sudo su
  102  history
ubuntu@Ansible-server:~$ ^C
ubuntu@Ansible-server:~$ ls
control-plane.yml  hosts  kube-cluster  kube-dependencies.yml  workers.yml
ubuntu@Ansible-server:~$ i control-plane.yml
i: command not found
ubuntu@Ansible-server:~$ vi control-plane.yml
ubuntu@Ansible-server:~$ vi hosts
ubuntu@Ansible-server:~$ vi kube-dependencies.yml
ubuntu@Ansible-server:~$ vi workers.yml
ubuntu@Ansible-server:~$ cd kube-cluster/
ubuntu@Ansible-server:~/kube-cluster$ ls
control-plane.yml  dependencies.yml  hosts  initial.yml  kube-dependencies.yml  setup_ssh.yml  workers.yml
ubuntu@Ansible-server:~/kube-cluster$ vi initial.yml
ubuntu@Ansible-server:~/kube-cluster$ vi setup_ssh.yml
ubuntu@Ansible-server:~/kube-cluster$ ^C
ubuntu@Ansible-server:~/kube-cluster$

