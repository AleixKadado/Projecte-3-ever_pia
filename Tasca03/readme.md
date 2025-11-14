# 📘 Guia de Configuració de LVM (Logical Volume Manager)

## 1️⃣ Configuració inicial

Primer, es crea una màquina virtual amb **Zorin OS**.

Amb la màquina apagada, afegim **dos discos de 10 GB** cadascun, que funcionaran com a unitats físiques addicionals.

Un cop iniciada la màquina, instal·lem l’eina `fdisk` per comprovar que els discos s’han afegit correctament:

```bash
sudo apt install fdisk
sudo fdisk -l
```

Observarem que, a més del disc principal (`sda`), apareixen els discos nous (`sdb` i `sdc`).

---

## 2️⃣ Creació dels volums físics (PV)

Instal·lem LVM:

```bash
sudo apt install lvm2
```

Creem els volums físics:

```bash
sudo pvcreate /dev/sdb
sudo pvcreate /dev/sdc
```

---

## 3️⃣ Creació del grup de volums (VG)

Unifiquem els discos físics dins d’un grup de volums:

```bash
sudo vgcreate volgrup /dev/sdb /dev/sdc
```

Podem verificar-lo amb:

```bash
sudo vgdisplay
```

---

## 4️⃣ Creació del volum lògic (LV)

Creem un LV de 200 MiB anomenat `lv01` dins del VG:

```bash
sudo lvcreate -L 200M -n lv01 volgrup
```

Amb `vgdisplay` podem veure l’espai utilitzat.

---

## 5️⃣ Formatació i muntatge del LV

Creem la carpeta de muntatge:

```bash
sudo mkdir /mnt/lv01
```

Formategem el volum en `ext4`:

```bash
sudo mkfs.ext4 /dev/volgrup/lv01
```

Muntem el volum:

```bash
sudo mount /dev/volgrup/lv01 /mnt/lv01
```

---

## 6️⃣ Muntatge persistent

Editem l’arxiu `/etc/fstab`:

```
/dev/volgrup/lv01 /mnt/lv01 ext4 defaults 0 0
```

Apliquem els canvis:

```bash
sudo mount -a
```

---

## 7️⃣ Alta disponibilitat (mirror)

El mirroring proporciona redundància similar a RAID 1.

### 7.0. Neteja prèvia

Primer desmuntem i eliminem el LV:

```bash
sudo umount /mnt/lv01
sudo lvremove /dev/volgrup/lv01
```

Eliminem l’entrada a `/etc/fstab` i després el grup de volums:

```bash
sudo vgremove volgrup
```

Comprovem l’estat dels volums físics:

```bash
sudo pvs
```

### 7.1. Creació del nou grup de volums per al mirror

```bash
sudo vgcreate vg_mirror /dev/sdb /dev/sdc
```

Creem un volum lògic en mirror:

```bash
sudo lvcreate -L 200M -m1 -n lv_mirror vg_mirror
```

Comprovació:

```bash
sudo lvs -a -o +devices | grep mirror
```

---

## 8️⃣ Instantànies (Snapshots)

Eliminem el LV anterior i creem un de nou de 100 MiB:

```bash
sudo lvremove /dev/volgrup/lv01
sudo lvcreate -L 100M -n lv01 volgrup
```

Formatem i muntem:

