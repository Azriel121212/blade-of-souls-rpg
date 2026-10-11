# ⚔️ Pixel Knight - 2D Action RPG

Sebuah game top-down 2D Action RPG bertema retro yang dibangun menggunakan **HTML5 Canvas**, **Vanilla JavaScript**, dan **Tailwind CSS**. Hadapi gelombang pasukan skeleton, tangkis proyektil sihir dengan pedang, kalahkan Boss raksasa di setiap level boss, dan tingkatkan status kesatriamu di Shop!

![HTML5](https://img.shields.io/badge/HTML5-Canvas-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)

---

## 🎮 Fitur Utama

- **🎵 Retro 8-Bit Chiptune BGM (Web Audio API Synthesizer)**:
  - Musik latar chiptune retro dinamis yang disintesis langsung menggunakan Web Audio API tanpa perlu file audio eksternal (`.mp3` / `.wav`).
  - Dua tema musik adaptif: **Explore Theme** (melodi petualangan santai saat menjelajah) dan **Boss Battle Theme** (tempo cepat, arpeggio agresif, dan drum kick/snare yang intens).
  - Dilengkapi tombol toggle `🔊 BGM` / `🔇 MUTED` di HUD kanan atas.
- **⚡ Quick Dash / Dodge Roll (<kbd>Shift</kbd> / Tombol Mobile)**:
  - Mekanik menghindar berkecepatan 3x burst speed lengkap dengan efek bayangan clone (*Ghost Trail*) berpendar cyan dan debu partikel.
  - Memberikan **Invulnerability Frames (i-Frames)** penuh selama manuver dash untuk menembus kepungan musuh dan proyektil.
  - Memiliki meteran cooldown responsif di layar HUD (`DASH [SHIFT]`).
- **👑 Epic Top Boss HUD Bar (Elden Ring / Dark Souls Style)**:
  - Bar darah widescreen megah di bagian atas layar dengan nama dinamis para Boss legendaris (*Lord Malakor Void Titan*, *Baron Ignis Flame Warden*, *King Oblivion Soul Eater*).
  - Menampilkan bar HP merah gradient dan bar Poise kuning Sekiro-style secara berdampingan.
  - Dilengkapi indikator lencana status pertempuran real-time seperti `💥 GUARD BROKEN!` dan `🔥 ENRAGED!`.
- **🗺️ Arena & Biome Progression (Perpindahan Lantai Dinamis)**:
  - Menghabisi Boss akan memicu transisi arena ke lantai berikutnya secara mulus disertai banner pengumuman:
    - **Floor 1: Whispering Forest** (lantai rumput hijau subur, pepohonan rimbun, semak belukar).
    - **Floor 2: Ancient Catacombs** (lantai ubin batu purba gelap `#15161d`, pilar-pilar batu berukir rune bercahaya cyan, obor menyala dengan api berkedip real-time).
    - **Floor 3: Volcanic Abyss** (kerak basalt lahar membara `#1a0b0b`, rekahan magma menyala, kristal obsidian tajam, dan kawah kawah geyser lava berbuih).
- **⚔️ 3-Hit Combo, Sword Wave & Parry Mechanic**:
  - **Sistem 3-Hit Combo**: Ayunan ke-1 & ke-2 adalah tebasan pedang melee cepat; ayunan ke-3 adalah **Finisher Blast** yang melepaskan **Sword Wave (Proyektil Sabit)** berkekuatan tinggi!
  - **🌊 Sword Wave (Proyektil Energi Sabit)**: Gelombang sabit energi yang menembus musuh, memukul mundur, dan dapat ditingkatkan hingga Triple Wave 3 arah di Shop.
  - **🌪️ Jangkauan Tebasan (AoE)**: Radius dan lebar tebasan pedang membesar secara visual dan hitbox.
  - **🛡️ Invulnerability Frames (i-Frames) & Iron Armor**: Jeda kebal sesaat saat terkena hit agar tidak mati instan saat dikerumuni monster.
  - **Mekanik Tangkis (Parry)**: Ayunan pedang bisa memantulkan bola sihir penyihir kembali ke musuh dengan damage balasan x3 lipat!
- **💀 Ekosistem Musuh Dinamis & Boss Battle**:
  - **🛡️ Shield Skeleton**: Membawa perisai di depan yang memantulkan/memblokir proyektil sabit! Harus ditebas dari samping/belakang atau dihancurkan dengan Skill [F].
  - **🐗 Charger / Dasher**: Musuh agresif yang memberi aba-aba sesaat lalu menerjang cepat (dash rush) lurus ke arah pemain.
  - **⭐ Elite Monsters (Lvl 6+)**: Muncul dengan aura emas berpendar, ukuran 1.35x, darah 2.5x lipat, tahan knockback, dan menjatuhkan 5 koin saat dikalahkan.
  - **🧙 Mage Skeleton**: Menyerang jarak jauh dengan proyektil terarah (drop 2 koin).
    - **⚔️ Boss Parry & Ping-Pong Rally ("Dead Man's Volley")**: Boss dapat menangkis (*parry*) serangan tebasan gelombang energi pemain dan memantulkannya kembali dengan aura merah membara berkecepatan tinggi! Pemain dapat menangkis balik gelombang tersebut secara ritmis (rally) untuk melipatgandakan kecepatan dan damage hingga salah satu terkena telak.
    - **🛡️ Boss Melee Clank**: Menyerang Boss dari jarak dekat memiliki risiko ditepis (*CLANK!*), menghasilkan percikan logam dan dorongan recoil mundur pada pemain.
  - **⚡ Sekiro-Style Poise / Stagger Meter (Rebalanced)**: Boss memiliki bar postur (*Poise 75*) di bawah bar HP. Memenangkan parry rally atau mendaratkan serangan (terutama Shadow Smash [F]) akan menguras Poise Boss secara agresif hingga pecah (**GUARD BROKEN! STAGGERED!** selama 2.5 detik, tertegun dan menerima **2x Critical Damage**). Poise kini dijamin pecah sebelum Boss mati sehingga pemain dapat menikmati jendela serangan kritikal!
    - **🔥 Boss Enrage Phase (< 30% HP)**: Saat sekarat, Boss mengamuk dengan aura api merah menyala, kecepatan gerak +35%, dan cooldown serangan Earthquake Stomp 2x lebih cepat.
    - **💥 Dynamic Screen Shake & Audio**: Getaran layar berbobot dan efek suara denting pedang (*parry ping*) dan *posture shatter*.
    - **Earthquake Stomp**: Menghentak tanah dan merambatkan cincin shockwave merah berbahaya.
    - **Minion Summon (Fase 50% HP)**: Mengaum dan memanggil 4 skeleton minion pengawal ke arena!
    - Hadiah kemenangan: 25 Koin, 2 Heart Potion, 1 Sword Upgrade, dan 1 **Mythic Soul Orb** (+350-500 XP)!
- **💎 Dynamic Leveling, Kill Streak & Soul Gems (Lvl 10-15+ Flow)**:
  - **Kurva XP yang Halus**: Kebutuhan XP level tinggi tidak lagi meledak eksponensial (1.4x), melainkan meningkat secara bertahap dan adil sehingga leveling di level 10-20+ tetap cepat dan memuaskan.
  - **Scaling XP Musuh**: XP yang didapat dari setiap monster otomatis meningkat seiring naiknya level pemain (+14% per level).
  - **⚡ Kill Streak Momentum**: Membunuh musuh secara beruntun dalam waktu singkat memicu pengganda XP (hingga +100% / 2x XP pada streak 6+).
  - **💎 Soul Gem & Mythic Orb**: Monster elite dan normal berpeluang menjatuhkan *Soul Gem* (`💎`), dan Boss menjatuhkan *Mythic Soul Orb* (`🔮`) yang otomatis tertarik magnet untuk percepatan XP masif!
- **🌲 Dinamika Lingkungan (Environment)**:
  - Pepohonan, pilar, obor, kristal obsidian, geyser lava, dan bebatuan menyesuaikan tema Biome yang aktif.
  - Efek transparansi otomatis saat karakter atau musuh berada di balik objek tinggi agar tidak menutupi aksi pertempuran.
- **🏪 Blacksmith Shop & Ekonomi Koin**:
  - 7 Pilihan Upgrade lengkap: Health Potion, Max HP Boost, Attack Damage, Sword Wave Proyektil, Blade Reach (AoE), Iron Armor (Def), dan Vampire Rune (Lifesteal HP per kill).
- **📱 Dukungan Desktop & Mobile**:
  - Kontrol keyboard responsif di PC/Laptop.
  - Tombol virtual D-Pad dan Action Button (ATK & DASH) yang otomatis aktif di layar smartphone / perangkat sentuh.

---

## 🕹️ Kontrol Permainan

### Desktop (Keyboard)
| Tombol | Aksi |
| :--- | :--- |
| <kbd>W</kbd> <kbd>A</kbd> <kbd>S</kbd> <kbd>D</kbd> / Tombol Panah | Bergerak (Atas, Kiri, Bawah, Kanan) |
| <kbd>Space</kbd> | Serang Pedang & Wave Proyektil (Sesuai arah hadap) |
| <kbd>Shift</kbd> | **Quick Dash / Dodge Roll** (i-Frames & Ghost Trail) |
| <kbd>F</kbd> | Super Magic Skill (AoE Nova) |
| <kbd>B</kbd> | Buka / Tutup Upgrade Shop |

### Mobile (Touchscreen)
- **D-Pad (Kiri bawah)**: Navigasi gerakan karakter.
- **Tombol DASH (Kanan bawah)**: Dash Dodge Roll kilat dengan i-frames.
- **Tombol ATK (Kanan bawah)**: Serang dengan pedang.
- **Tombol SHOP (Kanan atas)**: Akses upgrade shop.
- **Tombol 🔊 BGM (Kanan atas)**: Mute / Unmute musik latar.

---

## 🚀 Cara Menjalankan

Tidak memerlukan instalasi node_modules atau server rumit, game ini dapat langsung dimainkan di browser apa pun:

1. **Clone repository ini**:
   ```bash
   git clone https://github.com/Azriel121212/blade-of-souls-rpg.git
   ```
2. **Masuk ke folder proyek**:
   ```bash
   cd blade-of-souls-rpg
   ```
3. **Buka game**:
   - Cukup klik dua kali file `index.html`, atau
   - Buka dengan ekstensi **Live Server** di VS Code.

---

## 📁 Struktur File

```text
├── index.html         # Logika utama game, canvas rendering, & UI overlay
├── player.png         # Sprite sheet animasi karakter Player
├── boss.png           # Sprite sheet animasi Boss monster
├── entities.png       # Sprite sheet musuh (Skeleton Melee & Mage)
├── README.md          # Dokumentasi proyek
└── assets/            # Gambar pelengkap & artwork
```

---

## 🛠️ Dibangun Dengan

- **Canvas API (2D Context)** - Rendering game engine, partikel, dan animasi sprite berbasis frame time.
- **Vanilla JavaScript (OOP)** - Logika entitas, deteksi tabrakan (AABB circle/box collision), dan state management.
- **Tailwind CSS & Google Fonts ("Press Start 2P")** - Desain HUD retro modern.

---

## 📜 Lisensi
Proyek ini dibuat untuk keperluan pembelajaran dan pengembangan game web. Bebas dimodifikasi dan dikembangkan lebih lanjut!
