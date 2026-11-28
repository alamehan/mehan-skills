<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./assets/readme-header-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="./assets/readme-header-light.svg" />
    <img alt="Mehan Skills — @alamehan 2.5D kinetic banner" src="./assets/readme-header-light.svg" width="100%" />
  </picture>

  <p>
    <a href="./README.md">← English</a> · <strong>Bahasa Indonesia</strong>
    &nbsp;&nbsp;·&nbsp;&nbsp;
    <a href="./skills"><strong>✨ Lihat Daftar Skill</strong></a> ·
    <a href="https://alamehan.github.io">Portfolio</a> ·
    <a href="./LICENSE">Lisensi MIT</a>
  </p>
</div>

> ⚡ Playbook satu-file yang memandu AI menguji ide bebas bias, menjaga kualitas kode, merapikan repo & menulis dokumentasi — crafted by @alamehan
>
> `ai-agents` `agent-skills` `prompt-engineering` `claude-code` `cursor` `antigravity` `developer-tools` `software-quality`

---

## Kenapa Mehan Skills Dibuat

Setiap kali memulai proyek baru atau membuka sesi obrolan AI baru, mengulang standar kerja yang sama — bagaimana menguji ide agar bebas bias dan tidak kebablasan (*over-engineering*), memeriksa tampilan dan alur secara tuntas, merapikan struktur folder tanpa merusak fitur yang sudah jalan, hingga menyelaraskan seluruh dokumentasi sebelum rilis — memakan banyak waktu dan rawan melenceng kalau aturannya hanya tersimpan di riwayat chat lama.

**Mehan Skills** merangkum alur kerja Product Design dan Product Engineering dari **[M. Raihan Rafiiful Allaam (`@alamehan`)](https://alamehan.github.io)** ke dalam **buku panduan satu file yang praktis**. Setiap skill berdiri utuh di dalam satu file `.md` yang bisa langsung terbaca otomatis di seluruh ruang kerjamu, atau cukup dilampirkan kapan saja di chat AI pilihanmu.

---

## Langsung Lihat & Coba Sekarang

| Apa yang ingin kamu lakukan | Buka bagian ini |
|---|---|
| **Menguji ide tanpa bias, menggarap & melacak akar bug standar produksi, menjaga repo *evergreen*, *sync* dokumen & audit rilis `0%` memori (`playbook`)** | Buka **[`alamehan-playbook`](./skills/alamehan-playbook/SKILL.md)** |
| **Merapikan struktur folder proyek yang berantakan tanpa bikin error** | Buka **[`alamehan-repo-tidy`](./skills/alamehan-repo-tidy/SKILL.md)** |
| **Membuat halaman depan GitHub 2 bahasa yang ramah & beranimasi 2.5D** | Buka **[`alamehan-readme`](./skills/alamehan-readme/SKILL.md)** |
| **Melihat karya produk, design system & studi kasus `@alamehan` lainnya** | Kunjungi **[alamehan.github.io](https://alamehan.github.io)** |

---

## Keunggulan Utama

- **Cukup Satu File Utuh:** Setiap skill tersimpan lengkap di dalam satu file `SKILL.md` (berisi panduan, cetakan visual, hingga daftar pengecekan akhir) tanpa tercecer ke banyak file tambahan.
- **Playbook Kualitas Ideasi hingga Pra-Rilis (`alamehan-playbook`):** Cukup ketik `playbook` (atau sampaikan maksudmu seperti biasa) untuk memilih dari 12 situasi manusiawi — mulai dari uji ide *first principles* & rem anti-*over-engineering*, lacak akar bug/lag, cek layar Desktop/Mobile nyata, arsitektur *evergreen*, *sync* dokumen via `git diff`, hingga audit sesi baru `0%` memori.
- **Perapihan Repo Tanpa Waswas (`alamehan-repo-tidy`):** Memandu AI mengenali jalur penting lebih dulu, merapikan skrip dan folder yang kusut, memperbarui seluruh tautan kode yang ikut pindah, lalu memastikan aplikasi tetap berjalan mulus.
- **Dokumentasi Ramah Semua Kalangan (`alamehan-readme`):** Menyusun cerita pembuka yang jernih dengan tipografi desainer asli (`Bricolage Grotesque` + `Figtree` + `Geist Mono`), deskripsi *GitHub About* + *Topics* siap salin, serta panduan teknis developer di dalam laci lipat.
- **Fleksibel di Semua Alat AI:** Bisa dipasang otomatis secara global di Antigravity, maupun dilampirkan manual sebagai 1 file `.md` di Claude, ChatGPT, Cursor, atau Codex.

---

## Detail Teknis & Panduan Developer

<details>
<summary><strong>🛠️ Cara Pasang Cepat — Aktif Otomatis Global &amp; Lampiran Manual</strong></summary>

### Cara 1 · Aktif Otomatis di Semua Proyek Lokal (Antigravity / Gemini)
Kloning repositori ini satu kali, lalu hubungkan folder `./skills` ke `~/.gemini/config/skills` agar seluruh skill otomatis aktif di setiap proyekmu:

```powershell
# Windows PowerShell (tanpa perlu akses Administrator)
git clone https://github.com/alamehan/mehan-skills.git
cd mehan-skills
New-Item -ItemType Directory -Force -Path "$HOME\.gemini\config" | Out-Null
New-Item -ItemType Junction -Path "$HOME\.gemini\config\skills" -Target "$PWD\skills"
```

```bash
# macOS / Linux
git clone https://github.com/alamehan/mehan-skills.git
cd mehan-skills
mkdir -p "$HOME/.gemini/config"
ln -sfn "$PWD/skills" "$HOME/.gemini/config/skills"
```

### Cara 2 · Lampirkan Manual 1 File (Claude Web, ChatGPT, Cursor, Codex)
Lampirkan langsung 1 file `SKILL.md` dari folder [`skills/`](./skills) bersama repositori targetmu, lalu minta AI menjalankan panduannya.

</details>

<details>
<summary><strong>🏗️ Katalog Skill, Peta Arsitektur &amp; Struktur Folder</strong></summary>

```mermaid
flowchart LR
  vault["mehan-skills<br/>Gudang Skill Satu-File"] --> play["skills/alamehan-playbook/SKILL.md"]
  vault --> tidy["skills/alamehan-repo-tidy/SKILL.md"]
  vault --> rdm["skills/alamehan-readme/SKILL.md"]
  play --> global["~/.gemini/config/skills<br/>(Aktif Otomatis Global)"]
  tidy --> global
  rdm --> global
```

| Jalur | Peran |
|---|---|
| [`skills/alamehan-playbook/SKILL.md`](./skills/alamehan-playbook/SKILL.md) | Suite 12 playbook universal untuk uji ide bebas bias, debug akar masalah, cek layar responsif nyata, arsitektur *evergreen*, *sync* dokumen `git diff`, & audit rilis `0%` memori (`playbook`). |
| [`skills/alamehan-repo-tidy/SKILL.md`](./skills/alamehan-repo-tidy/SKILL.md) | Panduan merapikan struktur repositori secara menyeluruh dengan pelacakan referensi dan pembuktian build/tes. |
| [`skills/alamehan-readme/SKILL.md`](./skills/alamehan-readme/SKILL.md) | Cetakan banner SVG 2.5D `Porcelain SaaS` berfont desainer asli, kalimat *GitHub About*, dan standar kesetaraan 2 bahasa (`EN`/`ID`). |
| [`assets/`](./assets) | Banner panggung SVG 2.5D `@alamehan` bertema `Porcelain SaaS` versi Gelap dan Terang. |
| [`AGENTS.md`](./AGENTS.md) | Aturan baku penambahan skill baru (`1 Skill = 1 SKILL.md`, path universal, dan sinkronisasi katalog 2 bahasa). |

</details>

<details>
<summary><strong>🧭 Aturan Penulisan Skill &amp; Batasan Desain</strong></summary>

- **Murni 1 File per Skill:** Seluruh cetakan dan daftar periksa disertakan langsung di dalam `skills/<slug>/SKILL.md` agar tidak pernah rusak saat dibagikan atau dilampirkan ke chat web.
- **Bebas Path Spesifik Perangkat:** Semua contoh perintah memakai `$PWD` dan `$HOME` agar berjalan seragam di Windows, macOS, dan Linux. Baca [`AGENTS.md`](./AGENTS.md) saat ingin menambah skill baru.

</details>

---

Dirancang dan dibangun sepenuh hati oleh **[M. Raihan Rafiiful Allaam (`@alamehan`)](https://alamehan.github.io)** — *Product Designer & Product Engineer*. Dirilis di bawah [Lisensi MIT](./LICENSE).
