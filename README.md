# UNKNOWN (lngshot AU) - Recoded by Kyuu (t.me/kyunotdev)

> **Recode by Kyuu**: [t.me/kyunotdev](https://t.me/kyunotdev) | **Status Web:** Ampas Ilusi Doang 🤡

Repositori ini adalah hasil *recode* dan *crawling* aset/source code dari web fiksi interaktif AU (*Alternate Universe*) **"UNKNOWN (lngshot AU by hujan)"** yang aslinya mejeng di:
`https://lngshot-au-unknown.rinai.workers.dev/`

---

## 🧐 Web Ini Canggih? AMPAS BANGET, ILUSI DOANG!

Kalau lu liat sekilas di layar HP, web ini keliatan kayak simulasi iOS canggih yang dibikin sama *engineer* Silicon Valley bergaji ratusan juta. Tapi pas lu bedah jeroan *source code*-nya... **asli ampas, isinya cuma sulap tipu-tipu era dinosaurus.**

Mari kita preteli satu-satu kegoblokan dan ilusi di baliknya:

### 1. "Simulasi iPhone Canggih"? Bro, Cuma `<div>` Dikasih Border-Radius!
Lu kira ini bikin custom runtime WebAssembly atau virtualisasi OS? 
* **Realita**: Ini cuma satu tag `<div id="phone">` yang ditemplokin `border-radius: 56px` sama `box-shadow` segede gaban biar keliatan kayak bodi HP.
* Dynamic Island sama notch-nya? Cuma `div` hitam nempel di atas.
* Ikon sinyal 5G sama baterai? Cuma beberapa biji tag `<i>` yang tingginya dibedain. Bocah SMK baru belajar CSS sehari juga bisa bikin.

### 2. "Chat Interaktif Real-time"? Interaktif dari Hongkong!
Banyak bocah Twitter/TikTok takjub: *"Wah gila bisa ngetik balesan sendiri, AI-nya pinter banget!"*
* **Realita**: **GAK ADA AI, GAK ADA WEBSOCKET, GAK ADA OTAK.**
* Lu mau mencet tuts keyboard mana aja, mau lu ketik *"muka lu kayak toples peyek"*, teks yang nongol di layar **tetep teks skenario yang udah di-hardcode**. Lu cuma disuruh mencet keyboard doang kayak monyet sirkus buat memicu trigger script.
* Lawan chat lu bisa ngetik dan jeda? Cuma `setTimeout()` bertumpuk-tumpuk, bro! Logika percabangannya nol besar, jalan lurus kayak rel kereta Argo Bromo.

### 3. Database? Fitur Cloud? MIMPI!
* **Instagram Feed & Stories**: Bukan narik dari API atau database. Isinya cuma *hardcoded* array JSON manual di JavaScript. Capek-capek nulis manual kayak anak magang disuruh rekap struk belanjaan.
* **Aplikasi Notes & Gmail**: Cuma string teks panjang yang di-split per baris. Kalau web lu refresh, semua progres langsung ambyar balik ke titik nol karena gak ada state storage yang bener.

### 4. Efek Horornya: Modal Jumpscare Murahan
* Yang bikin tegang bukan kecanggihan grafis WebGL atau WebGPU, tapi cuma audio player biasa yang muter `knock_1.mp3` secara tiba-tiba sama browser API `navigator.vibrate(200)` biar HP lu getar-getar. Trik jadul era web jebakan Batman 2008!

### 5. Banyak Bug Awokawok: Kodingan Spageti Penuh Ranjau! 🐛🤡
Jangan kaget kalau pas nyoba mainin lu nemu error aneh-aneh:
* **Spam klik dikit langsung jebol**: Coba aja spam tombol *back*, tombol chat, atau tombol accept pas simulasi jalan. State script-nya langsung amnesia, audio ringtone numpuk-numpuk gak mau mati kayak speaker kondangan rusak awokawok!
* **Layar melar kayak karet kolor**: Buka di desktop terus resize window cepet-cepet, tampilan iPhone-nya bisa langsung gepeng kayak kelindes tronton.
* **Memory Leak Berjamaah**: `setInterval()` liar dan event listener dihambur-hamburkan tanpa ampun tanpa cleanup. Buka web ini 10 menit di HP kentang dijamin langsung anget kayak setrikaan.
* **Video Macet di iPhone**: Server aslinya gak ngerti Range Request, alhasil pengguna iOS Safari sering dapet video jumpscare yang stuck blank hitam doang.
* **Sekali Crash = Wassalam**: Gak ada error handling apalagi auto-save. Begitu script-nya nyangkut, kelar idup lu, harus refresh dan ngulang dari intro awokawok!

### 6. Kesimpulan Teknis:
Kodenya murni **Vanilla JavaScript spageti ~1.300 baris campur aduk** dalam satu file HTML tanpa framework (React/Vue/Svelte? Haram!), tanpa TypeScript, tanpa bundler. 

**Tapi ya harus diakui:** Meskipun kodenya ampas dan primitif, *gimmick*-nya sukses nipu netizen yang gampang takjub sama tampilan estetik ala iPhone.

---

## 📂 Struktur Aset yang Di-Crawl

```text
lngshot-au-unknown/
├── index.html         # 1.300+ baris kode spageti, skenario cerita, dan DOM mock iOS
├── style.css          # Ribuan baris CSS manual buat nipu mata biar keliatan kayak iPhone
├── server.py          # Python server darurat (karena SimpleHTTP bawaan Python ampas gak bisa muter video)
├── image/             # 73 aset gambar (dump foto, avatar, foto chat, lockscreen)
├── sfx/               # 17 sound effect (suara ketukan pintu, ringtone, napas, dll)
├── video/             # Video FaceTime jumpscare (vc.mov) & video files (210526.mp4)
└── README.md          # Dokumen tukang roasting ini
```

---

## 🚀 Cara Menjalankan (Biar Bisa Nipu Temen Lu Juga)

### Cara Bener (Pake `server.py`):
Karena browser HP (terutama Safari di iOS) manja banget dan nolak muter file video `.mov`/`.mp4` kalau servernya gak dukung *HTTP 206 Partial Content (Range Request)*, jalankan server Python custom ini:

```bash
cd /root/lngshot-au-unknown
python3 server.py
```

Buka di browser:
* **Lokal**: `http://localhost:8080`
* **Jaringan Luar / IP Publik**: `http://<IP-SERVER>:8080`

### Cara Males (Default Python):
```bash
python3 -m http.server 8080
```
*(Jangan komplain kalau video jumpscare FaceTime-nya ngadat/rusak di iPhone, server bawaan Python emang gak ada fitur Range Request).*
