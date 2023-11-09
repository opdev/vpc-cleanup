Ansible playbook to clean up the listed VPCs. The variable 'vpcs_to_remove' should be provided
in some fashion depending on the Ansible invocation.

Its contents should look like:

```yaml
vpcs_to_remove:
  - region: us-east-1
    vpcs:
      - foo-vpc
      - bar-vpc
  - region: us-east-2
    vpcs:
      - baz-vpc
```

Running locally 
```shell
ansible-playbook main.yml -e @extravars-sample.yml
```
