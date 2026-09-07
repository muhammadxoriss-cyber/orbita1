# Orbita — Biznes sayti

Statik HTML/CSS/JS sayt. Backend kerak emas — to'g'ridan-to'g'ri GitHub Pages, Vercel yoki Netlify'ga deploy qilish mumkin.

## Fayllar
- `index.html` — sahifa tuzilishi
- `style.css` — dizayn
- `script.js` — mobil menyu va forma logikasi

## VS Code'da ochish
1. Papkani VS Code'ga tashlang: `File → Open Folder`
2. "Live Server" kengaytmasini o'rnating va `index.html` ustida "Go Live" bosing (lokal ko'rish uchun)

## GitHub'ga push qilish
```bash
cd business-site
git init
git add .
git commit -m "Birinchi versiya: Orbita biznes sayti"
git branch -M main
git remote add origin https://github.com/USERNAME/REPO_NOMI.git
git push -u origin main
```
`USERNAME` va `REPO_NOMI`ni o'zingiznikiga almashtiring.

## Deploy qilish (bepul variantlar)

**GitHub Pages:**
1. Repo → Settings → Pages
2. "Branch" qismida `main` ni tanlang, papka: `/root`
3. Bir necha daqiqadan so'ng `https://USERNAME.github.io/REPO_NOMI/` manzilida ishga tushadi

**Vercel:**
1. vercel.com'ga GitHub akkaunt bilan kiring
2. "New Project" → repo'ni tanlang → Deploy (sozlamalarni o'zgartirish shart emas)

**Netlify:**
1. netlify.com → "Add new site" → "Import an existing project"
2. GitHub repo'ni tanlang → Deploy

## Tahrirlash uchun maslahatlar
- Kompaniya nomi va matnlar: `index.html` ichida
- Ranglar: `style.css` fayl boshidagi `:root` bo'limida (`--accent` asosiy rang)
- Aloqa formasi hozircha faqat demo — real xabar yuborish uchun Formspree yoki shunga o'xshash xizmatga ulash kerak bo'ladi
