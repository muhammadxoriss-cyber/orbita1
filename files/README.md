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

## Vercel'ga deploy qilish

Loyihada `vercel.json` fayli bor — bu statik sayt ekanini aniq belgilaydi, qo'shimcha build sozlamasi shart emas.

**1-usul: Vercel dashboard orqali (eng oson)**
1. GitHub'ga push qilib bo'lgach, [vercel.com](https://vercel.com)'ga GitHub akkaunt bilan kiring
2. "Add New..." → "Project" ni bosing
3. Repo'ingizni tanlang (`REPO_NOMI`)
4. Framework sifatida "Other" avtomatik aniqlanadi — hech narsani o'zgartirmasdan "Deploy" tugmasini bosing
5. Bir necha soniyada `https://REPO_NOMI.vercel.app` manzili tayyor bo'ladi

**2-usul: Vercel CLI orqali (GitHub'ga push qilmasdan ham ishlaydi)**
```bash
npm install -g vercel
cd business-site
vercel login
vercel --prod
```
Terminal savollariga javob bering (loyiha nomi, papka — default javoblar yetarli), va deploy avtomatik boshlanadi.

**Keyingi o'zgarishlarni chiqarish:**
- GitHub orqali bo'lsa: `git push` qilishning o'zi yetarli — Vercel avtomatik qayta deploy qiladi
- CLI orqali bo'lsa: har safar `vercel --prod` buyrug'ini qayta ishga tushiring

## Muqobil variantlar (agar kerak bo'lsa)

**GitHub Pages:**
1. Repo → Settings → Pages
2. "Branch" qismida `main` ni tanlang, papka: `/root`
3. Bir necha daqiqadan so'ng `https://USERNAME.github.io/REPO_NOMI/` manzilida ishga tushadi

**Netlify:**
1. netlify.com → "Add new site" → "Import an existing project"
2. GitHub repo'ni tanlang → Deploy

## Tahrirlash uchun maslahatlar
- Kompaniya nomi va matnlar: `index.html` ichida
- Ranglar: `style.css` fayl boshidagi `:root` bo'limida (`--accent` asosiy rang)
- Aloqa formasi hozircha faqat demo — real xabar yuborish uchun Formspree yoki shunga o'xshash xizmatga ulash kerak bo'ladi
