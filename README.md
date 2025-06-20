# PrivateVaults

PrivateVaults is a lightweight Bukkit/Spigot plugin that gives each player their own set of secure, persistent vaults.
Each vault is a private storage inventory that saves its contents automatically.
Instead of bloating a central config file, each vault is saved to its own YAML file under `plugins/PrivateVaults/vaults/`.

---

## 🚀 Features

* **`/pv <number>`**: Open a vault GUI. Sizes are configurable per vault (default 32 slots).
* **`/pv <number> <player>`**: (Admin only — requires `mamtak.pv.adminaccess`) Open another player’s vault.
* **`/pv list`**: List all vault numbers you can access.
* **`/pv list <player>`**: (Admin only — requires `mamtak.pv.adminaccess`) List another player’s vaults.
* **`/pv reload`**: (OP only) Reloads `config.yml` on the fly without restarting.

---

## 📥 Installation

1. Place the compiled JAR into your server’s `plugins/PrivateVaults/` folder.
2. Start or reload the server to generate the default `config.yml`.
3. Edit `plugins/PrivateVaults/config.yml` to customize vault limits & sizes.
4. Restart the server or run `/pv reload` as an OP to apply changes.

---

## ⚙️ Configuration

### Vault Limits (per permission tier)

```yaml
vault-limits:
  normal:    2    # mamtak.pv.normal
  advanced:  4    # mamtak.pv.advanced
  rich:      6    # mamtak.pv.rich
  moderator: 8    # mamtak.pv.moderator
  admin:    12    # mamtak.pv.admin
  owner:     0    # mamtak.pv.owner (0 = unlimited)
```

### Vault Sizes

```yaml
default-vault-size: 32  # must be a multiple of 9

vault-sizes:
  1: 32
  2: 32
  # add overrides per vault number
```

Vault data is stored per-player in separate files (`<UUID>_<vault#>.yml`), keeping your main config lightweight.

---

## 🔒 Permissions

| Permission              | Description                                 |
| ----------------------- | ------------------------------------------- |
| `mamtak.pv.normal`      | Access up to **vault-limits.normal** vaults |
| `mamtak.pv.advanced`    | Access up to **vault-limits.advanced**      |
| `mamtak.pv.rich`        | Access up to **vault-limits.rich**          |
| `mamtak.pv.moderator`   | Access up to **vault-limits.moderator**     |
| `mamtak.pv.admin`       | Access up to **vault-limits.admin**         |
| `mamtak.pv.owner`       | Access **unlimited** vaults (`owner: 0`)    |
| `mamtak.pv.adminaccess` | List/open other players’ vaults (OP only)   |

---

## 🛠 Compatibility

* **Spigot/Paper** 1.21.3+
* **Java** 17+
* **No external dependencies**

---

## 📄 License

This project is open source and free to use. Contributions and feedback welcome!

---

Happy vaulting! 🔐
