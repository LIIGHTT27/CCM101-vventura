# Checkpoint 6 – Technical Documentation
# Firewall Configuration

## 1. Allow SSH

The following command allows SSH connections so I can remotely access the server.

```bash
sudo ufw allow ssh
```

## 2. Default Deny Policy

These commands block all incoming connections by default while allowing outgoing connections.

```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

## 3. Allow Port 8080

This command allows TCP traffic through Port 8080, which is needed to access the web application.

```bash
sudo ufw allow 8080/tcp
```

## 4. What if `ufw enable` runs before `ufw allow ssh`?

If I run `sudo ufw enable` before `sudo ufw allow ssh`, my SSH connection may be blocked, causing me to lose remote access to the server.

## 5. Enable the Firewall

After configuring the firewall rules, I can enable UFW using:

```bash
sudo ufw enable
```

## 6. Verify Firewall Status

I can check the firewall status and active rules using:

```bash
sudo ufw status
```
