### Playbook
* Limit to host/group: `--limit "host/group"`
* Run with specific variables: `--extra-vars "key=value"`
* Run as different user: `-u <username>`
* Prompt for pass and sudo: `-kK`

### Ad-hoc
Get date/time for all hosts:
```
ansible all -a "date"
```
