# ansible-network-henrik-test


    $ ansible-playbook -i inventory/dev vlans2.yml
    [WARNING]: Ansible is being run in a world writable directory (/mnt/c/Tools/Ansible/First try), ignoring it as an ansible.cfg source. For more information see
    https://docs.ansible.com/ansible/devel/reference_appendices/config.html#cfg-in-world-writable-dir

    PLAY [add vlans] ****************************************************************************************************************************************************************************************************************

    TASK [debug] ********************************************************************************************************************************************************************************************************************
    ok: [kbh-pl6-lab.net.schibsted.se] => (item={'id': 888, 'name': 'vlan1'}) => {
        "msg": [
            "888",
            "vlan1"
        ]
    }
    ok: [kbh-pl6-lab.net.schibsted.se] => (item={'id': 889, 'name': 'vlan2'}) => {
        "msg": [
            "889",
            "vlan2"
        ]
    }

    TASK [debug] ********************************************************************************************************************************************************************************************************************
    ok: [kbh-pl6-lab.net.schibsted.se] => (item=- id: 888
    name: vlan1
    - id: 889
    name: vlan2) => {
        "msg": [
            "- id: 888\r\n   name: vlan1\r\n- id: 889\r\n  name: vlan2"
        ]
    }

    TASK [debug] ********************************************************************************************************************************************************************************************************************
    fatal: [kbh-pl6-lab.net.schibsted.se]: FAILED! => {"msg": "The task includes an option with an undefined variable. The error was: 'ansible.utils.unsafe_proxy.AnsibleUnsafeText object' has no attribute 'id'\n\nThe error appears to be in '/mnt/c/Tools/Ansible/First try/vlans2.yml': line 30, column 7, but may\nbe elsewhere in the file depending on the exact syntax problem.\n\nThe offending line appears to be:\n\n\n    - debug:\n      ^ here\n"}

    PLAY RECAP **********************************************************************************************************************************************************************************************************************
    kbh-pl6-lab.net.schibsted.se : ok=2    changed=0    unreachable=0    failed=1    skipped=0    rescued=0    ignored=0