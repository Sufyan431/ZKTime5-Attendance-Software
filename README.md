# ZKTeco Biometric Attendance Software

Is repository mein do ZKTeco attendance software hain. Agar ek kaam na kare to dusra use kar sakte hain.

---

## Software List

| Software | Folder | Version |
|----------|--------|---------|
| ZKTime 5.0 | `build153_ZKTeco/` | Build 153 |
| ZKBioTime.Net | `ZKBioTime_Net/` | 3.4.2.1 |

---

## ✅ ZKTeco Biometric Machine Reset Karne Ka Tarika
### (Jab IP Address Maloom Na Ho)

Aksar aisa hota hai ke biometric machine ka IP address pata nahi hota ya software se connect nahi hoti. Neeche diye gaye steps follow karein:

---

### 🔴 Method 1: Machine Ke Buttons Se Reset Karna (Sabse Aasaan)

1. **Machine band karein** (power off)
2. Machine ka **"Menu" button daba ke rakhen**
3. Dabay rakhtay huwey **power on karein**
4. Screen par **"Factory Reset"** ya **"Reset Settings"** ka option ayega
5. Woh select karein
6. Machine reset ho jayegi aur **default IP: `192.168.1.201`** set ho jayegi

> ⚠️ Default IP alag models mein alag ho sakta hai — neeche table dekhen

---

### 🔴 Method 2: Machine Ki Screen Se IP Dekhna / Change Karna

Agar machine mein screen hai (LCD/Touch):

1. **Menu** button dabain
2. **"Comm"** ya **"Communication"** mein jayein
3. **"Ethernet"** select karein
4. Wahan **IP Address** dikh jayega — note kar lein
5. IP change karna ho to wahan directly edit kar sakte hain

---

### 🔴 Method 3: USB Cable Se Direct Connect Karna

Agar network se connect nahi ho rahi:

1. Machine ko **USB cable** se computer se connect karein
2. ZKTime ya ZKBioTime software open karein
3. Software mein **"Add Device"** → **"USB Connection"** select karein
4. Machine automatically detect ho jayegi
5. Ab software se IP address set kar sakte hain

---

### 🔴 Method 4: Default IP Try Karna

Pehle yeh common default IPs try karein browser ya software mein:

| Model Type | Default IP |
|------------|------------|
| Zyadic / K40 / F18 | `192.168.1.201` |
| ZKBioTime machines | `192.168.1.201` |
| Purane models | `192.168.0.1` |
| Kuch models | `10.0.0.1` |

**Steps:**
1. Apne computer ka IP bhi usi range mein set karein
   - Masalan machine ka IP `192.168.1.201` hai to computer ka IP `192.168.1.100` karein
2. Browser mein `http://192.168.1.201` likhen
3. Default password: `admin` / `admin` ya `12345`

---

### 🔴 Method 5: Hard Reset (Sab Bhool Gaye Hoon Tab)

Agar kuch bhi kaam na kare — bilkul last option:

1. Machine ka **back panel** kholein
2. Ek chota sa **Reset button** hoga (pin se dabana padta hai)
3. Machine on hote huwey woh button **5-10 second** dabain
4. Machine factory settings par aa jayegi

---

### 📌 Reset Ke Baad Software Se Connect Karne Ka Tarika

**ZKTime 5.0:**
1. `build153_ZKTeco/setup.exe` install karein
2. Software open karein → **"Device"** → **"Add Device"**
3. IP address daalen (default: `192.168.1.201`)
4. Port: `4370`
5. **Connect** click karein ✅

**ZKBioTime.Net:**
1. `ZKBioTime_Net/Setup.exe` install karein
2. Software open karein → **"Device Management"** → **"Add"**
3. IP address aur port `4370` daalen
4. **Save & Connect** ✅

---

### ⚠️ Zaroori Baatain

- Reset karne se **saara data (attendance, fingerprints) delete** ho jayega
- Pehle data **backup** zaroor lein agar possible ho
- Machine aur computer **ek hi network** mein hone chahiye
- Firewall/Antivirus **port 4370** block na kare

---

## 📞 Madad chahiye?

Agar phir bhi machine connect na ho to in chezon ki photo share karein:
- Machine ka **model number** (peeche ya neeche likha hota hai)
- **Error message** jo aa raha hai

