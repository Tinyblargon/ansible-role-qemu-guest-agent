# Ansible Role: qemu_guest_agent

Ansible Role for installing qemu-guest-agent.

## Requirements

N/A

## Role Variables

| **Variable Name**      | **Type**| **Default Value**| **Description**|
| :----------------------| :------:| :---------------:| :--------------|
| qemu_guest_agent_state:| string  | "detect"         | This variable can be one of the following states `"absent"`, `"detect"`, `"latest"`, `"present"`. When `"absent"` the qemu-guest-agent package will be removed. When `"detect"` the package will be installed if the host has the virtual device required by the qemu-guest-agent, if the virtual device is absent the package will be removed. When `"latest"` the package will be installed or updated to the latest version. When `"present"` the package will be installed.|

## Example Playbooks

```yaml
- hosts: all
  roles:
    - role: tinyblargon.qemu_guest_agent
      vars:
        qemu_guest_agent_state: "present"
```

## License

MIT
