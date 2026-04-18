# Murat Aydıngüler İnşaat — Kurumsal Web Sitesi

Statik tanıtım sitesi. Sıfır bağımlılık, build adımı yok, GitHub Pages üzerinde yayınlanır.

## Yayınlama (GitHub Pages)

1. GitHub'da `murataydinguler.github.io` isminde **public** bir repo oluştur.
2. Bu klasörün içeriğini repo'ya push et.
3. Repo → **Settings → Pages → Source**: `main` branch / `/ (root)` seç → Save.
4. 1–2 dakika sonra `https://murataydinguler.github.io` adresinde yayında.

## Fotoğraf ekleme

Instagram sayfasından seçtiğin fotoğrafları indirip `images/projects/` klasörüne koy. Anlamlı dosya adları kullan:

```
images/projects/01-un-fabrikasi-konya.jpg
images/projects/02-makarna-fabrikasi-gaziantep.jpg
```

Ardından `index.html` içindeki `#projeler` bölümünde her kart için `src` yolunu güncelle. Örnek:

```html
<li><button type="button" class="gallery-item" data-src="images/projects/01-un-fabrikasi-konya.jpg">
  <img src="images/projects/01-un-fabrikasi-konya.jpg" alt="Konya un fabrikası — betonarme ana bina" loading="lazy">
</button></li>
```

Öneriler:
- Foto boyutu: genişlik **1200–1600px** arası, JPG, %80 kalite. 4:3 veya 3:2 en iyi sonuç.
- Dosya boyutu: tek foto **~300 KB** altında kalmalı.
- `alt` metni: projeyi tanımlayan kısa cümle (erişilebilirlik ve SEO için).

## Telefon / WhatsApp güncelleme

`index.html` içinde iki yer:

```html
<a class="btn btn-primary btn-lg" href="tel:+900000000000">
<a class="btn btn-whatsapp btn-lg" href="https://wa.me/900000000000" ...>
```

`+900000000000` kısmını firma numarasıyla değiştir (uluslararası format, başında `+` ve ülke kodu; WhatsApp linkinde `+` olmadan).

## Özel domain (ileride)

1. Repo kökünde `CNAME` isimli dosya oluştur, içine sadece domain yaz (ör: `aydingulerinsaat.com`).
2. Domain sağlayıcısında A kaydı olarak GitHub Pages IP'lerini, CNAME olarak `murataydinguler.github.io` ekle.
3. Settings → Pages → Custom domain alanında onayla, HTTPS'i etkinleştir.

## Yerel test

`index.html` dosyasına çift tıkla, tarayıcıda açılır. Tüm bölümler ve galeri dışarıda ek araç gerektirmez.
