# microsoft-iis-10-server-stig-hardening
# in progress

Windows Server 2019 system checks for DISA STIG compliancy. Findings are listed in the yml files in the tasks directory and are categorized in CAT I, CAT II, and CAT III according to the severities of each finding.

This is based on Windows Server 2019 DISA STIG implemtation guide: https://www.stigviewer.com/stig/microsoft_iis_10.0_server/2020-09-25/


The following packages must be installed on the controlling host/host where ansible is executed:
For many of the windows IIS modules, you must install the community.windows.collection Ansible plugin.
To install it use: ansible-galaxy collection install community.windows
To use it in a playbook, specify: community.windows.win_iis_website


To install it use: ansible-galaxy collection install ansible.windows.
To use it in a playbook, specify: ansible.windows.win_acl.


ansible-playbook -i inventory tasks/cat1.yml


Ansible from Linux (host) to Windows servers (peers), must install the following on the Windows servers for Ansible to execute this Role. 
- WinRM (review these for install) 
1) https://docs.ansible.com/ansible/latest/user_guide/windows_setup.html#winrm-setup
2) Run this ps1 script from cmd
https://raw.githubusercontent.com/ansible/ansible/devel/examples/scripts/ConfigureRemotingForAnsible.ps1
- IIS 

# Author: Gia Cao
# gcao@vmware.com
