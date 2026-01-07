# AWS EC2 + EBS Volume Management

## 📌 Project Overview
This project demonstrates:
- Launching a Linux EC2 instance
- Creating and attaching a 20 GB EBS volume
- Resizing the EBS volume and extending the filesystem

---

## 🛠 Technologies Used
- AWS EC2
- AWS EBS (gp3)
- Linux (Ubuntu / Amazon Linux)
- ext4 filesystem

---

## 🚀 Implementation Steps

### 1️⃣ Launch EC2 Instance
- Linux AMI
- Instance Type: t2.micro
- SSH access enabled

---

### 2️⃣ Create & Attach EBS Volume
- Volume Type: gp3
- Size: 20 GB
- Attached as `/dev/xvdf`

---

### 3️⃣ Configure Volume Inside EC2
```bash
lsblk
sudo mkfs.ext4 /dev/xvdf
sudo mkdir /data
sudo mount /dev/xvdf /data

