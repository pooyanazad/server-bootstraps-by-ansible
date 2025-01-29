# RedHat/CentOS

This playbook (`bootstrap-redhat_centos.yml`) quickly configures fresh RedHat or CentOS servers.

## Features
1. **System Updates** via `yum`
2. **New Sudo User** (no password required)
3. **SSH Key Deployment**
4. **Timezone** set to `Europe/Stockholm`
5. **DNS** changed to `8.8.8.8` and `8.8.4.4`
6. **Custom Aliases** (`ll`, `..`, `...`)
7. **firewalld** enabled, allowing SSH on port 22

## Usage

1. **Inventory**: Add your server to `inventory.ini` under `[redhat_hosts]`.
2. **Vars**: Adjust variables (username, timezone, etc.) in `bootstrap-redhat_centos.yml`.
3. **Run**:
   ```bash
   ansible-playbook -i inventory.ini bootstrap-redhat_centos.yml
   ```
4. **SSH**:
   ```bash
   ssh deployer@<server-ip>
   ```

Enjoy a consistent, time-saving setup for RedHat/CentOS systems!
