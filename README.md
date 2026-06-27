# 💗 Birlikteliğimiz

Kişisel ilişki sayacı — PWA (Progressive Web App).  
Telefon ana ekranına eklendiğinde tarayıcı çubuğu olmadan tam ekran çalışır.

## Dosya Yapısı

```
birlikteliğimiz/
├── index.html                    ← tüm uygulama kodu
├── photos.json                   ← arka plan fotoğraf listesi (buradan yönet)
├── bg1.jpg … bg7.jpg             ← arka plan fotoğrafları
├── apple-touch-icon.png          ← iPhone ana ekran ikonu (180×180)
├── favicon.svg                   ← tarayıcı sekme ikonu
├── favicon.ico                   ← eski tarayıcılar için
├── favicon-96x96.png             ← PNG favicon
├── web-app-manifest-192x192.png  ← Android ana ekran ikonu
├── web-app-manifest-512x512.png  ← Android splash / PWA ikonu
└── .gitignore
```

## Fotoğraf Ekle / Çıkar

Tüm fotoğraf yönetimi **`photos.json`** üzerinden yapılır — `index.html`'e dokunmana gerek yok.

1. Yeni fotoğrafı klasöre koy (örn. `yeni.jpg`)
2. `photos.json`'u aç ve adını ekle:
   ```json
   ["bg1.jpg", "bg2.jpg", "yeni.jpg"]
   ```
3. Dosyayı GitHub'a push'la → site otomatik güncellenir.

Çıkarmak için: dosyayı sil + `photos.json`'dan adını kaldır.

## Kişisel Ayarlar (`index.html` içinde)

```js
const BASLANGIC_TARIHI = "2023-06-15";   // ← ilişki başlangıç tarihi

const OZEL_GUNLER = [
  { ad: "Yıl Dönümümüz",     ay: 6,  gun: 15 },
  { ad: "Senin Doğum Günün", ay: 3,  gun: 22 },
  ...
];
```

## GitHub Pages ile Yayınlama

1. Repo → **Settings → Pages → Branch: main / root** → Save
2. `https://kullaniciadın.github.io/repo-adı` adresinde yayında!

## Ana Ekrana Ekleme (PWA)

**iPhone:** Safari → Paylaş → Ana Ekrana Ekle  
**Android:** Chrome → ⋮ → Ana ekrana ekle
