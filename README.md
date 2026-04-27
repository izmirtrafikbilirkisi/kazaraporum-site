# Adli Trafik Bilirkişisi Kazaraporum — Tanıtım Sitesi

Saf HTML + CSS + Vanilla JS ile yapılmış statik site. GitHub Pages üzerinde sunucusuz çalışır.

## Deploy (GitHub Pages)

1. GitHub'da yeni bir **public** repo oluşturun (örn. `kazaraporum-site`).
2. Bu klasörün içeriğini repoya push edin:
   ```bash
   git init
   git add .
   git commit -m "İlk yayın"
   git remote add origin https://github.com/KULLANICI_ADI/kazaraporum-site.git
   git push -u origin main
   ```
3. Repo **Settings → Pages → Source: `main` branch, `/ (root)`** seçin.
4. Birkaç dakika içinde `https://KULLANICI_ADI.github.io/kazaraporum-site/` adresinde yayınlanır.

## Özel Domain (İleride)

1. `CNAME` dosyasını repo kök dizinine oluşturun, içine domain adınızı yazın:
   ```
   kazaraporum.com
   ```
2. Domain DNS ayarlarınızda A kaydını GitHub Pages IP'lerine yönlendirin:
   ```
   185.199.108.153
   185.199.109.153
   185.199.110.153
   185.199.111.153
   ```

## Profil Fotoğrafı Ekleme

`assets/profile-placeholder.svg` dosyasını `assets/profile.jpg` ile değiştirin.
`index.html` içinde bu satırı güncelleyin:
```html
<img src="assets/profile-placeholder.svg" ...>
```
→
```html
<img src="assets/profile.jpg" ...>
```

## Google Analytics Ekleme

`index.html` içindeki `<!-- GA_TAG_PLACEHOLDER -->` yorumunu şununla değiştirin:
```html
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

## Yeni Makale Ekleme

1. `makaleler/trafik-kazasi-kusur-raporu-nasil-alinir.html` dosyasını kopyalayın.
2. İçeriği düzenleyin.
3. `makaleler/index.html` dosyasına yeni kartı ekleyin.
4. `sitemap.xml` dosyasına yeni URL'yi ekleyin.

## Lokal Test

```bash
python -m http.server 8080
```
Ardından `http://localhost:8080` adresini açın.
