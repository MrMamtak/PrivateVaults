# PrivateVaults

PrivateVaults is a lightweight Bukkit/Spigot plugin that gives each player their own set of secure, persistent vaults.  
Each vault is a private storage inventory (bigger than an Ender Chest) that saves its contents automatically.  
Instead of bloating a central config file, each vault is saved to its own YAML file under `plugins/PrivateVaults/vaults/`.  

---

## 🚀 Features
- **/pv <number>** command to open a vault GUI with 54 slots.
- Vault count is fully configurable by permission in `config.yml`:
  - `vault-limits.normal: 2`
  - `vault-limits.advanced: 4`
  - `vault-limits.rich: 6`
  - `vault-limits.moderator: 8`
  - `vault-limits.admin: 12`
  - `vault-limits.owner: 0` (infinite)
- Vault data is stored per-player, per-vault (`<UUID>_<vault#>.yml`).
- `/pv reload` lets OPs reload config on-the-fly (no server restart needed).

---

## 📥 Installation
1. Download the plugin JAR and place it into your server’s `plugins` folder.
2. Start the server to generate the default `config.yml`.
3. Edit `plugins/PrivateVaults/config.yml` to customize vault limits.
4. Restart the server or run `/pv reload` as OP to apply changes.

---

## 🔒 Permissions
| Permission              | Description |
|--------------------------|-------------|
| `mamtak.pv.normal`        | Allows up to vault-limits.normal (default: 2) |
| `mamtak.pv.advanced`      | Allows up to vault-limits.advanced (default: 4) |
| `mamtak.pv.rich`          | Allows up to vault-limits.rich (default: 6) |
| `mamtak.pv.moderator`     | Allows up to vault-limits.moderator (default: 8) |
| `mamtak.pv.admin`         | Allows up to vault-limits.admin (default: 12) |
| `mamtak.pv.owner`         | Allows infinite vaults (vault-limits.owner = 0) |


---

## 🛠 Compatibility
- Spigot/Paper 1.21.3+
- No external dependencies required

---

## 📄 License
This project is open source and free to use.

---

Happy vaulting! 🔐
