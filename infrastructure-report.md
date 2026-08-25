# 🖥️ Infrastructure Report
### *Cloud Infrastructure Assessment — CloudNova Technologies*

> **Client Brief:** A small company is preparing to migrate its services to the cloud. Before any servers are deployed, this report documents the current environment so senior engineers can design the final architecture.

---

## 📋 Server Snapshot

| 🔎 Attribute | 📝 Value |
|---|---|
| **Operating System** | Ubuntu 24.04.4 LTS (Noble Numbat) |
| **Kernel Version** | 6.8.0-138-generic |
| **CPU Model** | Intel Xeon E312xx (Sandy Bridge, IBRS update) |
| **CPU Core Count** | 1 |
| **Total RAM** | 1.9 GiB |
| **Disk Capacity** | 19 GiB (root partition `/`) |
| **Hostname** | ubuntu |
| **IP Address** | 172.30.1.2 (primary), 172.17.0.1 (secondary/docker bridge) |

---

## 💾 Operating System
> `cat /etc/os-release`

```
PRETTY_NAME="Ubuntu 24.04.4 LTS"
NAME="Ubuntu"
VERSION_ID="24.04"
VERSION="24.04.4 LTS (Noble Numbat)"
VERSION_CODENAME=noble
ID=ubuntu
ID_LIKE=debian
```

---

## 🧬 Kernel Version
> `uname -r`

```
6.8.0-138-generic
```

---

## ⚙️ CPU Model & Core Count
> `lscpu | grep "Model name"` and `nproc`

```
Model name:                         Intel Xeon E312xx (Sandy Bridge, IBRS update)
BIOS Model name:                    RHEL-9.6.0 PC (Q35 + ICH9, 2009)  CPU @ 2.0GHz
```

```
nproc
1
```

**Summary:** The server runs a single virtual CPU core based on an emulated Intel Xeon E312xx (Sandy Bridge) processor, running at 2.0 GHz. This is a minimal/lightweight allocation typical of a lab or sandbox environment rather than a production-grade server.

---

## 🧠 Total RAM
> `free -h`

```
              total        used        free      shared  buff/cache   available
Mem:           1.9Gi       419Mi       851Mi       1.1Mi       800Mi       1.4Gi
Swap:          1.0Gi          0B       1.0Gi
```

**Summary:** The server has approximately 1.9 GiB of total RAM, with 1.4 GiB currently available. A 1.0 GiB swap partition is configured but unused.

---

## 📦 Disk Capacity
> `df -h`

```
Filesystem      Size  Used Avail Use% Mounted on
tmpfs           191M  996K  190M   1%  /run
/dev/vda1        19G  5.4G   13G  30%  /
tmpfs           952M   84K  952M   1%  /dev/shm
tmpfs           5.0M     0  5.0M   0%  /run/lock
/dev/vda16      881M  117M  703M  15%  /boot
/dev/vda15      105M  6.2M   99M   6%  /boot/efi
```

**Summary:** The root filesystem (`/dev/vda1`) has a total capacity of 19 GiB, with 5.4 GiB used (30%) and 13 GiB still available.

---

## 🗂️ Mounted File Systems
> `mount | grep "^/dev"`

```
/dev/vda1 on / type ext4 (rw,relatime,discard,errors=remount-ro,commit=30)
/dev/vda16 on /boot type ext4 (rw,relatime)
/dev/vda15 on /boot/efi type vfat (rw,relatime,fmask=0077,dmask=0077,codepage=437,iocharset=iso8859-1,shortname=mixed,errors=remount-ro)
```

**Summary:** Three device-backed filesystems are mounted: the root filesystem (`/`) and `/boot` are formatted as `ext4`, while the EFI system partition (`/boot/efi`) uses `vfat`, which is standard for UEFI boot partitions.

---

## 🏷️ Hostname
> `hostname`

```
ubuntu
```

---

## 🌐 IP Address
> `hostname -I`

```
172.30.1.2 172.17.0.1
```

**Summary:** The server has two assigned IP addresses — `172.30.1.2`, its primary internal network address, and `172.17.0.1`, which corresponds to the default Docker bridge network interface.

---

## ✅ Assessment Notes
This server is provisioned as a lightweight sandbox environment: a single CPU core, ~1.9 GiB of RAM, and a 19 GiB root disk with healthy free space (70% available). This is sufficient for learning, testing, and running small services, but would need to be scaled up (additional CPU cores, more RAM, larger disk) before hosting a production workload for an actual client migration.

---
📁 *Part of the [CCM101 Cloud Computing Portfolio](../../README.md) — Laboratory 2: Build the Cloud Infrastructure Blueprint*

