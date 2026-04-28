# ZKTeco Biometric Attendance Software

This repository contains two ZKTeco attendance software. If one does not work, you can use the other.

---

## Software List

| Software | Folder | Version |
|----------|--------|---------|
| ZKTime 5.0 | `build153_ZKTeco/` | Build 153 |
| ZKBioTime.Net | `ZKBioTime_Net/` | 3.4.2.1 |

---

## ✅ How to Reset ZKTeco Biometric Machine
### (When IP Address is Unknown)

This is a common issue when the biometric machine's IP address is unknown or the software cannot connect to the device. Follow the steps below:

---

### 🔴 Method 1: Reset Using Machine Buttons (Easiest)

1. **Turn off the machine** (power off)
2. Press and **hold the "Menu" button**
3. While holding, **turn the power on**
4. **"Factory Reset"** or **"Reset Settings"** option will appear on screen
5. Select it
6. Machine will reset and **default IP: `192.168.1.201`** will be set

> ⚠️ Default IP may vary by model — see table below

---

### 🔴 Method 2: View / Change IP From Machine Screen

If the machine has an LCD/Touch screen:

1. Press the **Menu** button
2. Go to **"Comm"** or **"Communication"**
3. Select **"Ethernet"**
4. The **IP Address** will be visible — note it down
5. You can directly edit the IP from here if needed

---

### 🔴 Method 3: Connect Directly Via USB Cable

If the machine cannot connect over the network:

1. Connect the machine to the computer using a **USB cable**
2. Open ZKTime or ZKBioTime software
3. In software go to **"Add Device"** → **"USB Connection"**
4. Machine will be automatically detected
5. You can now set the IP address through the software

---

### 🔴 Method 4: Try Default IP Address

First try these common default IPs in your browser or software:

| Model Type | Default IP |
|------------|------------|
| Zyadic / K40 / F18 | `192.168.1.201` |
| ZKBioTime machines | `192.168.1.201` |
| Older models | `192.168.0.1` |
| Some models | `10.0.0.1` |

**Steps:**
1. Set your computer IP to the same range as the machine
   - Example: if machine IP is `192.168.1.201`, set computer IP to `192.168.1.100`
2. Type `http://192.168.1.201` in your browser
3. Default password: `admin` / `admin` or `12345`

---

### 🔴 Method 5: Hard Reset (Last Resort)

If nothing works — use this as the absolute last option:

1. Open the **back panel** of the machine
2. There will be a small **Reset button** (press with a pin)
3. While machine is ON, press and hold that button for **5-10 seconds**
4. Machine will restore to factory settings

---

### 📌 How to Connect Software After Reset

**ZKTime 5.0:**
1. Install `build153_ZKTeco/setup.exe`
2. Open software → **"Device"** → **"Add Device"**
3. Enter IP address (default: `192.168.1.201`)
4. Port: `4370`
5. Click **Connect** ✅

**ZKBioTime.Net:**
1. Install `ZKBioTime_Net/Setup.exe`
2. Open software → **"Device Management"** → **"Add"**
3. Enter IP address and port `4370`
4. Click **Save & Connect** ✅

---

### ⚠️ Important Notes

- Resetting the machine will **delete all data (attendance records, fingerprints)**
- Always take a **backup** of data before resetting if possible
- The machine and computer must be on the **same network**
- Make sure your Firewall/Antivirus is not blocking **port 4370**

---

## 📞 Need Help?

If the machine still does not connect, please share:
- Machine **model number** (written on the back or bottom)
- **Error message** you are receiving


---

## 🔌 How to Connect Biometric Machine Via LAN Cable

### Hardware Setup:
1. Plug one end of the LAN cable into the **biometric machine**
2. Plug the other end into your **computer or switch**

---

### ⚠️ Important: Turn Off WiFi / Internet

You **must turn off WiFi** before connecting via LAN cable.

**Why?**
If both WiFi and LAN are active, the computer gets confused about which network to use and the machine will not connect properly.

**Steps:**
1. **Turn off WiFi** on your computer
2. Only keep the **LAN cable connected** (machine → computer)

---

### Set Manual IP on Computer

1. Go to **Control Panel** → **Network and Sharing Center**
2. Click on **"Change adapter settings"**
3. Right-click on **Local Area Connection (Ethernet)** → **Properties**
4. Select **"Internet Protocol Version 4 (TCP/IPv4)"** → **Properties**
5. Select **"Use the following IP address"** and enter:
   - IP Address: `192.168.1.100`
   - Subnet Mask: `255.255.255.0`
   - Default Gateway: `192.168.1.1`
6. Click **OK** ✅

---

### Check Machine IP Address

1. Press **Menu** button on the machine
2. Go to **Comm** → **Ethernet**
3. Note down the **IP Address** shown on screen
4. Make sure machine IP and computer IP are in the **same range**
   - Example: Machine = `192.168.1.201`, Computer = `192.168.1.100` ✅

---

### Add Machine in Software

**ZKTime 5.0:**
1. Open software → **Device** → **Add Device**
2. Enter machine IP (e.g. `192.168.1.201`)
3. Port: `4370`
4. Click **Connect** ✅

**ZKBioTime.Net:**
1. Open software → **Device Management** → **Add**
2. Enter machine IP and Port `4370`
3. Click **Save & Connect** ✅

---

### Reset Machine From Software

Once machine is connected in software:
1. Go to **Device** → **Select your machine**
2. Click **"Reset Device"** or **"Clear Data"**
3. Confirm → Machine will reset ✅

> ⚠️ Resetting will delete all fingerprints and attendance data. Take backup first if needed.


---

## 📌 What is Port 4370?

- Port 4370 is the **default communication port** of all ZKTeco machines
- ZKTeco has fixed this port for all their devices
- You must always enter **4370** in the software when adding a device
- Without this port number, software cannot communicate with the machine

---

## 📶 Is it Necessary to Turn Off WiFi?

It depends on how you have connected the machine:

**Case 1: Machine connected via Router or Switch**
1. Connect LAN cable from machine to router/switch
2. Connect computer to the same router/switch
3. WiFi can remain ON ✅
4. Both devices are on the same network automatically

**Case 2: Machine connected directly to Computer (No Router)**
1. Connect LAN cable directly from machine to computer
2. **Turn off WiFi** on your computer
3. Set manual IP on computer (same range as machine)
4. Now connect via software ✅
5. WiFi must be OFF in this case to avoid network conflict ⚠️

---

## 🌐 Why Same IP Range is Necessary? (Step by Step)

Think of IP address like a home address — if street numbers are different, they cannot find each other.

**Step 1:** Check machine IP address
- Press **Menu** on machine → **Comm** → **Ethernet**
- Note the IP shown e.g. `192.168.1.201`

**Step 2:** Understand the IP range
- IP has 4 parts: `192` . `168` . `1` . `201`
- First 3 parts = Network range (must be same)
- Last part = Device number (must be different)

**Step 3:** Set computer IP in same range
- Go to **Control Panel** → **Network** → **Ethernet** → **Properties**
- Set IP: `192.168.1.100` (first 3 parts same, last part different)
- Subnet Mask: `255.255.255.0`
- Click **OK** ✅

**Step 4:** Verify
| Device | IP Address | Result |
|--------|------------|--------|
| Machine | `192.168.1.201` | - |
| Computer | `192.168.1.100` | ✅ Will Connect |
| Computer | `192.168.0.5` | ❌ Will NOT Connect |
| Computer | `10.0.0.1` | ❌ Will NOT Connect |

**Step 5:** Test connection
- Open **Command Prompt** (cmd)
- Type: `ping 192.168.1.201`
- If you get a reply → Machine is reachable ✅
- If "Request timed out" → Check IP range or cable ❌


---

## 🔌 How to Reset Biometric Machine Via LAN Cable (Step by Step)

### Step 1: Hardware Connection
1. Plug one end of LAN cable into the **biometric machine**
2. Plug the other end into your **computer**

---

### Step 2: Turn Off WiFi
1. Go to **System Tray** (bottom right)
2. Click on **WiFi icon**
3. Turn **WiFi Off** ✅
4. Only LAN cable should be active

---

### Step 3: Set Manual IP on Computer
1. Go to **Control Panel** → **Network and Sharing Center**
2. Click **"Change adapter settings"**
3. Right-click on **Ethernet / Local Area Connection** → **Properties**
4. Select **"Internet Protocol Version 4 (TCP/IPv4)"** → **Properties**
5. Select **"Use the following IP address"** and enter:
   - IP Address: `192.168.1.100`
   - Subnet Mask: `255.255.255.0`
   - Default Gateway: `192.168.1.1`
6. Click **OK** ✅

---

### Step 4: Check Machine IP Address
1. Press **Menu** button on the machine
2. Go to **Comm** → **Ethernet**
3. Note down the IP Address shown on screen
   - Example: `192.168.1.201`

---

### Step 5: Test Connection
1. Open **Command Prompt** (Press `Windows + R` → type `cmd` → Enter)
2. Type: `ping 192.168.1.201` and press Enter
3. If you get a **reply** → Connection is OK ✅
4. If **"Request timed out"** → Check cable or IP range ❌

---

### Step 6: Add Machine in Software

**ZKTime 5.0:**
1. Open software → **Device** → **Add Device**
2. Enter IP: `192.168.1.201`
3. Port: `4370`
4. Click **Connect** ✅

**ZKBioTime.Net:**
1. Open software → **Device Management** → **Add**
2. Enter IP: `192.168.1.201`
3. Port: `4370`
4. Click **Save & Connect** ✅

---

### Step 7: Reset Machine From Software
1. In software, select your connected device
2. Go to **Device** → **Reset Device** or **Clear Data**
3. Click **Confirm** ✅
4. Machine will restart and reset to factory settings

> ⚠️ All fingerprints and attendance records will be deleted after reset. Take backup first if needed.

