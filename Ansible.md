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

### Roles
#### Template role
`roles/logger/tasks/main.yml`
```yml
- name: Template task
  template:
	src: source.j2
	dest: "{{ logger.path }}"
  when: logger is defined
  tags: log-tag
```
`roles/other_role/tasks/main.yml`
```yml
- name: Configure logger
  include_role:
	name: logger
	apply:
	  tags: log-tag
  vars:
	logger:
	  path: /my/path
```
