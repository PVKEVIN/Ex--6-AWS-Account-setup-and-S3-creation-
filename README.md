# CLOUD STORAGE CREATION (S3) AND LAUNCHING AN (EC2) INSTANCE IN AWS
## NAME: Kevin P
## REG NO: 212224040159
## Aim

To create and configure an Amazon Elastic Block Store (EBS) volume, attach and mount it to an Amazon EC2 instance, create a snapshot backup, and restore the snapshot to a new EBS volume.

---

## Algorithm / Steps

1. Create a new Amazon EBS volume with a size of 1 GiB.
2. Select the same Availability Zone as the EC2 instance.
3. Attach the EBS volume to the EC2 instance using `/dev/sdb`.
4. Connect to the EC2 instance using AWS Systems Manager Session Manager.
5. Check the available storage using `df -h`.
6. Create an `ext3` file system on the EBS volume.
7. Create the `/mnt/data-store` directory.
8. Mount the EBS volume to `/mnt/data-store`.
9. Configure `/etc/fstab` for automatic mounting.
10. Verify that the EBS volume is successfully mounted.
11. Create `file.txt` inside the mounted EBS volume.
12. Verify the contents of the created file.
13. Create an EBS snapshot named `My Snapshot`.
14. Delete `file.txt` from the original EBS volume.
15. Create a new EBS volume from the snapshot.
16. Attach the restored volume to the EC2 instance using `/dev/sdc`.
17. Create the `/mnt/data-store2` directory.
18. Mount the restored volume to `/mnt/data-store2`.
19. Verify that `file.txt` has been successfully restored.

---

## Program

### 1. Check Available Storage

```bash
df -h
```

### 2. Create an ext3 File System

```bash
sudo mkfs -t ext3 /dev/sdb
```

### 3. Create a Mount Directory

```bash
sudo mkdir /mnt/data-store
```

### 4. Mount the EBS Volume

```bash
sudo mount /dev/sdb /mnt/data-store
```

### 5. Configure Automatic Mounting

```bash
echo "/dev/sdb   /mnt/data-store ext3 defaults,noatime 1 2" | sudo tee -a /etc/fstab
```

### 6. View the File System Configuration

```bash
cat /etc/fstab
```

### 7. Verify the Mounted Volume

```bash
df -h
```

### 8. Create a File in the EBS Volume

```bash
sudo sh -c "echo some text has been written > /mnt/data-store/file.txt"
```

### 9. Read the File

```bash
cat /mnt/data-store/file.txt
```

### 10. Delete the File

```bash
sudo rm /mnt/data-store/file.txt
```

### 11. Verify File Deletion

```bash
ls /mnt/data-store/
```

### 12. Create a Mount Directory for the Restored Volume

```bash
sudo mkdir /mnt/data-store2
```

### 13. Mount the Restored EBS Volume

```bash
sudo mount /dev/sdc /mnt/data-store2
```

### 14. Verify Snapshot Restoration

```bash
ls /mnt/data-store2/
```

Expected output:

```text
file.txt
```

---

## Outputs

### Output 1: EBS Volume Created

The AWS EC2 Volumes page shows the newly created `My Volume` EBS volume with a size of 1 GiB.
<img width="2556" height="1600" alt="Screenshot 2026-07-28 084203" src="https://github.com/user-attachments/assets/622bd161-cf4b-4a2f-b52a-787acdec576c" />



---

### Output 2: EBS Volume Attached to EC2 Instance

The `My Volume` EBS volume is successfully attached to the `Lab` EC2 instance and is in the `In-use` state.

<img width="2556" height="1596" alt="Screenshot 2026-07-28 084647" src="https://github.com/user-attachments/assets/c1c99206-310f-46ab-a0e5-4cf7539c8b9a" />


---

### Output 3: EBS Volume Mounted Successfully

The `df -h` command displays the mounted EBS volume at `/mnt/data-store`.


<img width="2534" height="1380" alt="image" src="https://github.com/user-attachments/assets/06fcc18e-45ab-443c-9684-7f72a116488b" />


---

### Output 4: File Created and Verified

The file `file.txt` is successfully created inside the EBS volume and the stored text is displayed.

```text
some text has been written
```

<img width="2560" height="1596" alt="Screenshot 2026-07-28 084824" src="https://github.com/user-attachments/assets/e0414096-fe24-4412-8332-1b7d1e240e0a" />



---

### Output 5: EBS Snapshot Created

The AWS EC2 Snapshots page shows `My Snapshot` with the snapshot creation completed successfully.
<img width="2558" height="1598" alt="Screenshot 2026-07-28 084124" src="https://github.com/user-attachments/assets/8c314377-8d01-4027-b37e-2302419e6271" />





---

### Output 6: Snapshot Restored Successfully

The snapshot is restored to a new EBS volume named `Restored Volume`. After attaching and mounting the restored volume, the deleted `file.txt` is successfully recovered.
```text
file.txt
```
<img width="2560" height="1596" alt="Screenshot 2026-07-28 084824" src="https://github.com/user-attachments/assets/698a0a51-6ff2-428e-9b57-9c410addc588" />


<img width="1917" height="1152" alt="Screenshot 2026-07-28 090515" src="https://github.com/user-attachments/assets/f501d053-c47a-4414-a445-1b8656bc755c" />
<img width="1917" height="1160" alt="Screenshot 2026-07-28 092957" src="https://github.com/user-attachments/assets/d411d29c-0ac7-406b-8556-394e1543667c" />

## Result
Thus, an Amazon EBS volume was successfully created and attached to an Amazon EC2 instance. The volume was formatted with an ext3 file system, mounted, and used for storing data. An EBS snapshot was successfully created as a backup, and a new EBS volume was restored from the snapshot. The previously deleted file.txt was successfully recovered, demonstrating the backup and restore functionality of Amazon EBS.
