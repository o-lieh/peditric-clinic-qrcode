# صفحه لینک کلینیک — راهنمای دیپلوی روی GitHub Pages

## ۱. جایگزینی محتوا (قبل از دیپلوی)
همه‌ی جاهایی که باید عوض کنی با کامنت `<!-- PLACEHOLDER: ... -->` داخل `index.html` مشخص شده‌اند:
- لینک کانال بله
- لینک رزرو نوبت دکترتو
- دو شماره تلفن (`tel:0000000000`)
- متن آدرس
- لینک نقشه نشان / بله / گوگل‌مپ
- لینک اینستاگرام
- لینک سایت کلینیک
- شماره تماس بله در پایین صفحه

## ۲. ساخت ریپازیتوری و دیپلوی
```bash
git init
git add index.html README.md
git commit -m "clinic link page"
git branch -M main
git remote add origin https://github.com/USERNAME/REPO_NAME.git
git push -u origin main
```

سپس در GitHub:
1. برو به **Settings > Pages**
2. زیر **Build and deployment > Source** گزینه‌ی **Deploy from a branch** را انتخاب کن
3. Branch را روی `main` و فولدر را روی `/ (root)` بگذار و **Save** بزن
4. بعد از چند دقیقه، آدرس صفحه این شکلی می‌شود:
   `https://USERNAME.github.io/REPO_NAME/`

اگر می‌خواهی آدرس کوتاه‌تر باشد، ریپازیتوری را با نام `USERNAME.github.io` بساز؛ در این حالت آدرس نهایی می‌شود:
`https://USERNAME.github.io/`

## ۳. ساخت QR Code
بعد از این‌که لینک نهایی فعال شد:
- از یک سرویس رایگان مثل qr-code-generator.com یا از دستور زیر (نیازمند پکیج `qrencode`) استفاده کن:
```bash
qrencode -o clinic-qr.png -s 10 "https://USERNAME.github.io/REPO_NAME/"
```
- برای چاپ، نسخه‌ی PNG یا SVG با کیفیت بالا (حداقل ۳۰۰ dpi) بگیر تا در سایز کارت یا استند مطب واضح باشد.

## نکات
- فونت از Google Fonts لود می‌شود (Vazirmatn)؛ برای کارکرد آفلاین کامل، می‌توان فونت را لوکال کرد — در صورت نیاز بگو تا اضافه کنم.
- صفحه responsive است و روی موبایل (که اکثر اسکن‌های QR از آن‌جا می‌آید) تست شده.
