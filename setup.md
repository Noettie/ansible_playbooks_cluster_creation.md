- hosts: all
  remote_user: root
  vars:
    authorized_key_list:
      - name: root
        authorized_keys:
         - key: "{{ lookup('file', '~/.ssh/id_rsa.pub') }}"
           state: present
  roles:
    - { role: GROG.authorized-key }
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
"setup_ssh.yml" [readonly] 10L, 241B                   
