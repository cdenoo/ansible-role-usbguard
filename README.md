# Ansible Role: USBGuard

[USBGuard Documentation](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/security_guide/sec-using-usbguard)

## Requirements

None

## Role Variables

| Variable                              | Default                              | Description                                     |
| :------------------------------------ | :----------------------------------- | :---------------------------------------------- |
| usbguard_rulefile                     | /etc/usbguard/rules.conf             | Location of the usbguard file containing rules  |
| usbguard_ImplicitPolicyTarget         | block                                | Default policy to be enforced                   |
| usbguard_PresentDevicePolicy          | apply-policy                         | Policy to be applied to already present devices |
| usbguard_PresentControllerPolicy      | keep                                 | Policy to be applied to controllers             |
| usbguard_InsertedDevicePolicy         | apply-policy                         |                                                 |
| usbguard_RestoreControllerDeviceState | false                                |                                                 |
| usbguard_DeviceManagerBackend         | uevent                               |                                                 |
| usbguard_IPCAllowedUsers              | root                                 |                                                 |
| usbguard_IPCAllowedGroups             | ""                                   |                                                 |
| usbguard_IPCAccessControlFiles        | /etc/usbguard/IPCAccessControl.d/    |                                                 |
| usbguard_DeviceRulesWithPort          | false                                |                                                 |
| usbguard_AuditBackend                 | FileAudit                            |                                                 |
| usbguard_AuditFilePath                | /var/log/usbguard/usbguard-audit.log |                                                 |

## Dependencies

None

## Example Playbook

```
- hosts: server
  roles:
    - cdenoo.usbguard
```

## License

[MIT](https://opensource.org/licenses/MIT)/[BSD](https://opensource.org/licenses/BSD-3-Clause)

## Author Information

This role was created in 2019 by [Cedric Denoo](https://github.com/cdenoo)