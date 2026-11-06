# Portfolio – Vivaldi Adventus Simangunsong

Situs portfolio statis (HTML + CSS, tanpa build). Setiap `git push` ke branch `main` otomatis ter-deploy ke GitHub Pages lewat GitHub Actions.

## Deploy otomatis gratis (GitHub Pages)

1. Buat repo baru di GitHub (public), misalnya `vivaldiAS.github.io` (alamat situs: `https://vivaldias.github.io`) atau nama lain seperti `portfolio` (alamat: `https://vivaldias.github.io/portfolio/`).
2. Upload semua isi folder ini ke repo (termasuk folder `.github` dan `assets`):
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/vivaldiAS/NAMA-REPO.git
   git push -u origin main
   ```
3. Di GitHub: **Settings → Pages → Build and deployment → Source: GitHub Actions**.
4. Buka tab **Actions** dan tunggu workflow "Deploy portfolio to GitHub Pages" selesai (hijau). URL situs muncul di ringkasan job.

Setelah itu, cukup edit `index.html` lalu `git push`; situs ter-update sendiri dalam satu sampai dua menit.

## Struktur

- `index.html`: seluruh isi dan gaya situs
- `assets/profile.jpg`: foto profil
- `.github/workflows/pages.yml`: workflow deploy otomatis
- `.nojekyll`: supaya GitHub Pages menyajikan file apa adanya

## Alternatif gratis lain

Netlify, Cloudflare Pages, dan Vercel juga auto-deploy dari repo GitHub. Pilih repo ini, kosongkan build command, dan set publish directory ke `.` (root).
