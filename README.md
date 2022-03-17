Run it like this:

```
ansible-playbook playbook.yaml  -i hosts.yaml
```

Expected output:

```

PLAY [all] *********************************************************************

TASK [debug] *******************************************************************
ok: [node0] => {
    "firewall_rules": [
        "allow icmp",
        "allow port 22",
        "allow port 80",
        "allow port 443"
    ]
}
ok: [node1] => {
    "firewall_rules": [
        "allow icmp",
        "allow port 22",
        "allow port 3306"
    ]
}

PLAY RECAP *********************************************************************
node0                      : ok=1    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   
node1                      : ok=1    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   

```
