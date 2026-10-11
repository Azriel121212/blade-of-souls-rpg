# ⚔️ Pixel Knight - 2D Action RPG

Sebuah game top-down 2D Action RPG bertema retro yang dibangun menggunakan **HTML5 Canvas**, **Vanilla JavaScript**, dan **Tailwind CSS**. Hadapi gelombang pasukan skeleton, tangkis proyektil sihir dengan pedang, kalahkan Boss raksasa di setiap level boss, dan tingkatkan status kesatriamu di Shop!

![HTML5](https://img.shields.io/badge/HTML5-Canvas-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)

---

## 🎮 Fitur Utama

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
  - Pepohonan, semak-semak, dan bebatuan tersebar acak di arena.
  - Efek transparansi otomatis saat karakter atau musuh berada di balik pepohonan agar tidak menutupi aksi pertempuran.
- **🏪 Blacksmith Shop & Ekonomi Koin**:
  - 7 Pilihan Upgrade lengkap: Health Potion, Max HP Boost, Attack Damage, Sword Wave Proyektil, Blade Reach (AoE), Iron Armor (Def), dan Vampire Rune (Lifesteal HP per kill).
- **📱 Dukungan Desktop & Mobile**:
  - Kontrol keyboard responsif di PC/Laptop.
  - Tombol virtual D-Pad dan Action Button yang otomatis aktif di layar smartphone / perangkat sentuh.
- **✨ Visual & Efek Partikel**:
  - Tebasan glowing neon cyan & white core yang membesar sesuai level upgrade.
  - Floating damage text (merah untuk damage player, kuning untuk damage musuh, hijau untuk heal/vampire, ungu untuk parry).
  - Partikel percikan darah, pecahan proyektil, dan transisi bar HP/XP yang halus.

---

## 🕹️ Kontrol Permainan

### Desktop (Keyboard)
| Tombol | Aksi |
| :--- | :--- |
| <kbd>W</kbd> <kbd>A</kbd> <kbd>S</kbd> <kbd>D</kbd> / Tombol Panah | Bergerak (Atas, Kiri, Bawah, Kanan) |
| <kbd>Space</kbd> | Serang dengan Pedang (Sesuai arah hadap) |
| <kbd>F</kbd> | Dash / Skill Khusus |
| <kbd>B</kbd> | Buka / Tutup Upgrade Shop |

### Mobile (Touchscreen)
- **D-Pad (Kiri bawah)**: Navigasi gerakan karakter.
- **Tombol ATK (Kanan bawah)**: Serang.
- **Tombol SHOP (Kanan atas)**: Akses upgrade shop.

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
