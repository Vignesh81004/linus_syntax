Here you go! Below is a clean, **practice-ready command list** for **Linux System Monitoring** and **Mounting**, written in a simple and general format—perfect for saving to GitHub as a reference.

---

# **Linux System Monitoring – Practice Commands**

## **CPU & Memory Monitoring**

### **1. top — Real-time system monitoring**

```bash
top
```

### **2. htop — Interactive process viewer**

(Install first if needed)

```bash
sudo apt install htop
htop
```

### **3. vmstat — CPU, memory, I/O stats**

```bash
vmstat 1 5       # refresh every 1 sec, total 5 updates
```

### **4. free — Check memory usage**

```bash
free -m          # show usage in MB
```

---

## **Disk Monitoring**

### **1. df — Check disk space**

```bash
df -h
```

### **2. du — Check directory size**

```bash
du -sh /var/log
du -sh /home/user
```

### **3. iostat — Disk + CPU stats**

(Install sysstat if missing)

```bash
sudo apt install sysstat
iostat
```

---

## **Network Monitoring**

### **1. View network interfaces**

```bash
ip a
```

### **2. Check open ports**

```bash
netstat -tulnp
ss -tulnp
```

### **3. Test connectivity**

```bash
ping google.com
traceroute google.com
```

### **4. DNS lookup**

```bash
nslookup example.com
```

---

## **Log Monitoring**

### **1. Live system logs**

```bash
tail -f /var/log/syslog
journalctl -f
```

### **2. Kernel logs**

```bash
dmesg | tail
```

---

# **Linux Mounting Commands – Practice Commands**

Here are the **commonly used mounting commands** you can practice:

### **1. Check existing mounted file systems**

```bash
mount
lsblk
```

### **2. Create a mount point**

```bash
sudo mkdir /mnt/mydrive
```

### **3. Mount a device**

Example: mount `/dev/sdb1`

```bash
sudo mount /dev/sdb1 /mnt/mydrive
```

### **4. Unmount a device**

```bash
sudo umount /mnt/mydrive
```

### **5. Auto-mount entries (view /etc/fstab)**

```bash
cat /etc/fstab
```

### **6. Mount all entries from /etc/fstab**

```bash
sudo mount -a
```

### **7. Check file system type**

```bash
sudo blkid
```

---

