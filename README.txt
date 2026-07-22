WANZZ DEPLOY — Cara Pakai (Demo)
=================================

1. Buka file config.js dengan text editor.
2. Ganti nilai placeholder dengan token demo kamu:

   window.WANZZ_CONFIG = {
     githubUser:   "wanzz25",
     githubToken:  "isi_token_github_demo_kamu",
     vercelToken:  "isi_token_vercel_demo_kamu",
     netlifyToken: "isi_token_netlify_demo_kamu",
   };

3. Simpan file, lalu buka index.html di browser (double click,
   atau jalankan local server misal: python3 -m http.server).

4. Kalau nanti ganti token demo, tinggal edit config.js lagi
   dan refresh browser — tidak perlu sentuh file lain.

PENTING — KEAMANAN
-------------------
- config.js JANGAN diupload ke GitHub, hosting publik, atau
  dikirim ke orang lain. File ini isinya kredensial mentah.
- Kalau project ini di-push ke Git, tambahkan baris berikut
  ke .gitignore:

      config.js

- File ini tetap berjalan di browser (client-side), jadi siapa
  pun yang buka halaman lewat "View Page Source" bisa melihat
  isi config.js. Cocok untuk demo lokal/terbatas saja — untuk
  publik/production, key harus dipindah ke backend/server
  (environment variable), bukan file frontend.
- Status "CONNECTED / READY TO USE" di dashboard hanya
  tampilan UI berdasarkan config.js — proses deploy di
  script.js tetap simulasi (log animasi), belum memanggil
  API GitHub/Vercel/Netlify yang sesungguhnya.
