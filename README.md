# 🏠 My Workspace — Portal Kerja Pribadi

Website pribadi berbasis MkDocs untuk manajemen notula, agenda, tugas, dan arsip kerja.

---

## 📦 Struktur Folder

```
my-workspace/
├── docs/
│   ├── index.md                  ← Beranda utama
│   ├── notula/
│   │   ├── index.md              ← Daftar semua notula
│   │   └── template-notula.md   ← Template notula rapat
│   ├── agenda/
│   │   ├── index.md              ← Jadwal bulanan
│   │   └── template-agenda.md   ← Template agenda kegiatan
│   ├── tasks/
│   │   ├── index.md              ← Task tracker utama
│   │   └── template-tasks.md    ← Template detail tugas
│   ├── catatan/
│   │   ├── index.md              ← Jurnal & catatan
│   │   └── template-catatan.md  ← Template catatan harian
│   └── arsip/
│       └── index.md              ← Arsip & referensi
├── mkdocs.yml                    ← Konfigurasi MkDocs
└── README.md                     ← File ini
```

---

## 🚀 Cara Setup di GitHub Pages

### 1. Buat Repository
```
Nama repository: my-workspace (atau sesuai keinginan)
Visibility: Private (direkomendasikan)
```

### 2. Upload semua file ke repository

### 3. Aktifkan GitHub Pages dengan GitHub Actions
Buat file `.github/workflows/deploy.yml` dengan isi:

```yaml
name: Deploy MkDocs
on:
  push:
    branches: [main]
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: actions/setup-python@v4
        with:
          python-version: '3.x'
      - run: pip install mkdocs-material
      - run: mkdocs gh-deploy --force
```

### 4. Website Anda akan aktif di:
```
https://[username].github.io/[nama-repository]/
```

---

## ✏️ Cara Mengedit Konten

**Cara termudah (langsung di browser):**
1. Buka file `.md` yang ingin diedit di GitHub
2. Klik ikon pensil ✏️
3. Edit konten
4. Scroll ke bawah → klik **Commit changes**
5. Website otomatis update dalam 1–2 menit

**Cara menggunakan template:**
1. Buka template yang sesuai (misalnya `template-notula.md`)
2. Buat file baru di folder yang sama
3. Salin isi template → isi datanya
4. Commit

---

## 📝 Panduan Format Markdown Cepat

| Format | Markdown | Hasil |
|---|---|---|
| Tebal | `**teks**` | **teks** |
| Miring | `*teks*` | *teks* |
| Checklist | `- [ ] tugas` | ☐ tugas |
| Checklist ✅ | `- [x] tugas` | ☑ tugas |
| Tabel | `\| A \| B \|` | Tabel |
| Heading | `## Judul` | Judul besar |

---

*Dibuat dengan ❤️ menggunakan MkDocs + Material Theme*
