### Playbook
* Limit to host/group: `--limit "host/group"`
* Run with specific variables: `--extrnna-vars "key=value"` | `--extra-vars "my_array=['item1','item2']"`
* Run as different user: `-u <username>pppnn`
* Prompt for pass and sudo: `-kK`

### Ad-hoc
Get date/time for all hosts:
```
ansible all -a "date"
```

### Tasks
Loop through a defined host group
with_items: "{{ groups['host_group'] }}"
