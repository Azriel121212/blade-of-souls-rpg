# ⚔️ Pixel Knight - 2D Action RPG

Sebuah game top-down 2D Action RPG bertema retro yang dibangun menggunakan **HTML5 Canvas**, **Vanilla JavaScript**, dan **Tailwind CSS**. Hadapi gelombang pasukan skeleton, tangkis proyektil sihir dengan pedang, kalahkan Boss raksasa di setiap level boss, dan tingkatkan status kesatriamu di Shop!

![HTML5](https://img.shields.io/badge/HTML5-Canvas-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)

---

## 🎮 Fitur Utama

- **⚔️ 4-Directional Combat, Sword Wave & Parry Mechanic**:
  - Serangan tebasan pedang berjarak dekat sesuai arah hadap karakter.
  - **🌊 Sword Wave (Proyektil Energi Sabit)**: Tiap ayunan pedang meluncurkan gelombang sabit energi yang menembus dan menghantam musuh dari jarak jauh (dapat ditingkatkan hingga Triple Wave 3 arah!).
  - **🌪️ Jangkauan Tebasan (AoE)**: Radius dan lebar tebasan pedang dapat ditingkatkan secara visual dan hitbox-nya.
  - **🛡️ Invulnerability Frames (i-Frames) & Iron Armor**: Pemain mendapatkan jeda kebal sesaat saat terkena hit agar tidak langsung mati instan saat dikerumuni, serta dapat membeli perlindungan Armor pengurang damage.
  - **Mekanik Tangkis (Parry)**: Ayunan pedang bisa memantulkan bola sihir musuh kembali ke arah mereka dan memberikan damage balasan x3 lipat!
- **💀 Variasi Musuh & Boss Battle**:
  - **Melee Skeleton & Bat**: Mengejar dan menyerang pemain.
  - **Mage Skeleton**: Menyerang dari jarak jauh menggunakan bola sihir terarah (drop 2 koin).
  - **Epic Boss Monster**: Muncul setiap kelipatan level 5 dengan animasi sprite sheet lengkap, drop 25 koin, guaranteed heart & sword!
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
