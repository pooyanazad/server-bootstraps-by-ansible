# Ubuntu

This playbook (`bootstrap-ubuntu.yml`) automates the initial configuration of Ubuntu or Debian-based servers.

## Features
1. **System Updates**: `apt update && apt upgrade`
2. **New Sudo User** (no password required)
3. **SSH Key Deployment**
4. **Timezone** set to `Europe/Stockholm`
5. **DNS** changed to `8.8.8.8` and `8.8.4.4`
6. **Custom Aliases** (`ll`, `..`, `...`)
7. **UFW Firewall** with port 22 open

## Usage

1. **Inventory**: Add your server to `inventory.ini` under `[ubuntu_hosts]`.
2. **Vars**: Adjust variables (username, timezone, etc.) in `bootstrap-ubuntu.yml`.
3. **Run**:
   ```bash
   ansible-playbook -i inventory.ini bootstrap-ubuntu.yml
   ```
4. **SSH**:
   ```bash
   ssh deployer@<server-ip>
   ```

Feel free to remove or modify tasks to match your exact needs.
