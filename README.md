# 🤖 Marketing Agent

AI Marketing Agent dengan fitur Ads, SEO, Copywriting, Ide Konten, dan Analisis — tersimpan otomatis ke Google Sheets.

## Fitur
- 📢 **Ads** — Generate copy iklan untuk berbagai platform
- 🔍 **SEO** — Optimasi konten & keyword
- ✍️ **Copywriting** — Headline, email, caption, tagline
- 💡 **Ide Konten** — Brainstorm konten 5–30 ide
- 📊 **Analisis** — Analisis kompetitor & strategi
- 🗂️ **Data Produk** — Simpan & baca data produk dari Google Sheets

## Deploy ke Vercel

### 1. Upload ke GitHub
1. Buka [github.com](https://github.com) → klik **+** → **New repository**
2. Beri nama: `marketing-agent`
3. Pilih **Public** → klik **Create repository**
4. Di halaman berikutnya, klik **uploading an existing file**
5. Upload semua file dari folder ini
6. Klik **Commit changes**

### 2. Deploy ke Vercel
1. Buka [vercel.com](https://vercel.com) → **Add New Project**
2. Pilih repository `marketing-agent` dari GitHub
3. Klik **Environment Variables** dan tambahkan:

| Key | Value |
|-----|-------|
| `ANTHROPIC_API_KEY` | API key dari console.anthropic.com |
| `GOOGLE_CLIENT_EMAIL` | `marketing-agent@moonlit-triumph-498912-j2.iam.gserviceaccount.com` |
| `GOOGLE_PRIVATE_KEY` | Isi dengan isi private_key dari file JSON (copy seluruhnya termasuk `-----BEGIN...-----END-----`) |
| `GOOGLE_SHEET_ID` | `156FSZUoUabIKoUGe530eXMPG3nkUshTG6H7QC0ciLXs` |

4. Klik **Deploy** → tunggu 1-2 menit → dapat link!

### ⚠️ Catatan penting untuk GOOGLE_PRIVATE_KEY
Saat input di Vercel, paste nilai private_key dari file JSON persis seperti ada di file JSON (dengan `\n` di dalamnya). Vercel akan handle otomatis.

## Environment Variables (.env.local untuk development lokal)
```
ANTHROPIC_API_KEY=your_key
GOOGLE_CLIENT_EMAIL=marketing-agent@moonlit-triumph-498912-j2.iam.gserviceaccount.com
GOOGLE_PRIVATE_KEY="-----BEGIN PRIVATE KEY-----\n...\n-----END PRIVATE KEY-----\n"
GOOGLE_SHEET_ID=156FSZUoUabIKoUGe530eXMPG3nkUshTG6H7QC0ciLXs
```
