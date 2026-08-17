# Хуримын урилга (веб урилга)

Энэ бол `index.html` дотор бүрэн бичигдсэн, ямар ч сервер шаардахгүй, GitHub Pages дээр үнэгүй байршуулж болох веб урилга.

## Файлын бүтэц

```
urilga-repo/
├── index.html      ← бүх код (HTML+CSS+JS) энд байна
├── photos/          ← гэрлэн зургаа энд хийнэ
├── music/            ← дэвсгэр хөгжмөө энд хийнэ
└── README.md
```

## 1. Юуг хэрхэн засах вэ

`index.html` файлыг нээгээд **`CONFIG`** гэсэн хэсгийг хайж олоорой (Ctrl+F → "ЗАСВАРЛАХ ГАЗАР"). Тэнд:

- **Нэр, огноо, цаг, хаяг, Google Maps линк** — шууд текстээр бичигдсэн
- **`heroPhotoUrl`** — гэрлэн зургаа `photos/` хавтсанд хуулаад жишээ нь `photos/hero.jpg` гэж бич
- **`audioSrc`** — дуугаа `music/` хавтсанд хуулаад жишээ нь `music/song.mp3` гэж бич

Шүлгийн бичвэрүүд (`Хүндэт зочинд`, `Ураг холбон барилдах`, төгсгөлийн мөр) нь HTML дотор шууд бичигдсэн бөгөөд `<!-- ЗАСВАРЛАХ -->` гэсэн тайлбарын дараа байрлана.

## 2. GitHub дээр байршуулах бүрэн дараалал

### Алхам 1 — GitHub дээр шинэ repository үүсгэх
1. https://github.com/new хаягаар ор
2. Repository name: жишээ нь `urilga`
3. **Public** сонгоод "Create repository" дар

### Алхам 2 — Энэ хавтсыг өөрийн компьютер руу татаж, git-ээр push хийх
Доорх командуудыг ажлын хавтсандаа (`urilga-repo`) орж ажиллуул. `YOUR_USERNAME`-г өөрийн GitHub нэрээр сол:

```bash
cd urilga-repo
git init
git add .
git commit -m "Хуримын урилга - анхны хувилбар"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/urilga.git
git push -u origin main
```

> Push хийхэд GitHub нэвтрэх мэдээлэл (эсвэл Personal Access Token) асууна. Нууц үгээ биш, **токен** ашиглана — https://github.com/settings/tokens дээрээс үүсгэнэ.

### Алхам 3 — GitHub Pages идэвхжүүлэх (үнэгүй сайт болгож нийтлэх)
1. Repo дотроо **Settings → Pages** руу ор
2. "Branch" хэсэгт `main` сонгоод, folder-г `/ (root)` болгоод **Save**
3. Хэдэн минутын дараа сайт чинь идэвхжинэ:
   ```
   https://YOUR_USERNAME.github.io/urilga/
   ```

### Алхам 4 — Дараа нь өөрчлөлт хийх бүрдээ
```bash
git add .
git commit -m "Мэдээлэл шинэчлэв"
git push
```
Хэдэн секундын дараа сайт чинь автоматаар шинэчлэгдэнэ.

## 3. Локал компьютер дээрээ шалгаж үзэх

Push хийхээсээ өмнө `index.html`-ийг браузераар шууд нээгээд харж болно (интернэт холболт шаардахгүй, зөвхөн Google Maps товч л онлайн орчинд ажиллана).
