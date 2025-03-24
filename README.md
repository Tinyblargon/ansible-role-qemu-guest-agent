# Ansible Role: qemu_guest_agent

Ansible Role for installing qemu-guest-agent.

## Requirements

N/A

## Role Variables

| **Variable Name**      | **Type**| **Default Value**| **Description**|
| :----------------------| :------:| :---------------:| :--------------|
| qemu_guest_agent_state:| string  | "present-auto"   | Defines the installation state of qemu-guest-agent. Possible values:<br> `"present"` – Ensures the package is installed.<br> `"present-auto"` - Installs the package only if the host has the required virtual device; it remains installed even if the device is later removed.<br> `"auto"` – Installs the package if the required virtual device is present; removes it if the device is absent.<br> `"latest"` – Installs or updates the package to the latest version.<br> `"absent"` – Ensures the package is removed.|

## Example Playbooks

```yaml
- hosts: all
  roles:
    - role: tinyblargon.qemu_guest_agent
      vars:
        qemu_guest_agent_state: "present-auto"
```

## License

MIT
