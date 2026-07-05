# Apikültür Vakfı — Web Sitesi

Apikültür Vakfı'nın resmî web sitesi. **Doğayı Geleceğe Taşır.**

Canlı adres (geçici): **https://vtknightmare.github.io/apikultur-vakfi/**
(apikulturvakfi.com bağlandığında güncellenecek)

## Yapı

Tek dosyalık statik bir site — derleme adımı, framework ya da bağımlılık yok.

| Dosya | İçerik |
|---|---|
| `index.html` | Sitenin tamamı: içerik, stil (inline CSS), davranış (vanilla JS), TR/EN çeviri sözlükleri |
| `senet.html` | Vakıf senedinin tam metni (yazdırılabilir; PDF: `assets/vakif-senedi.pdf`) |
| `assets/` | favicon, apple-touch-icon, og-image, senet PDF'i |
| `assets/img/` | Bölüm ve proje fotoğrafları |
| `robots.txt`, `sitemap.xml` | Arama motoru dosyaları |

İçerik kaynağı: `Apikultur_Vakfi_Site_Metni.docx` (final taslak, Alican). Marka kuralları: `ApiKultur-BrandGuidline_2026.pdf`. Hukuki kaynak: `apikültür vakıf senedi son.docx`.

**Logo:** Apimaye "A" rozeti — `APIMAYE_brandbook_2025-1.pdf` içindeki vektörden birebir alınmıştır (sarı #FFC828 + beyaz; oran ve renkler değiştirilemez). `assets/img/kurucu-aile.jpg` da aynı brandbook'tan kırpılmıştır; orijinal fotoğraf dosyası geldiğinde aynı adla değiştirilebilir.

**Fotoğraflar:** Unsplash'ten telifsizdir (Unsplash License — ticari kullanım serbest, atıf zorunlu değil; fotoğrafçılar: Vitaly Gariev, Toru Wa, Bernd Dittrich, Bianca Ackermann, Annie Spratt, Damien Tupinier, HiveBoxx, Arwin Neil Baichoo, Andrew Ridley). Vakfın kendi saha fotoğrafları hazır olduğunda `assets/img/` altındaki dosyalar aynı adlarla değiştirilebilir.

## Güncelleme

1. `index.html` içinde ilgili metni düzenleyin. **Dikkat:** Görünen metinlerin çoğu sayfa gövdesinde *ve* `<script>` içindeki `I18N` sözlüğünde (TR + EN) yer alır — ikisini de güncelleyin, yoksa dil değiştirildiğinde eski metin geri gelir.
2. `main` dalına commit + push yapın. GitHub Pages otomatik olarak yeniden yayınlar (1-2 dk).

## Alan adı bağlanacağı zaman

1. Repo → Settings → Pages → Custom domain: `apikulturvakfi.com` (CNAME dosyası otomatik oluşur)
2. DNS: `A` kayıtları → GitHub Pages IP'leri, `www` → CNAME `vtknightmare.github.io`
3. `index.html` içindeki canonical / `og:url` / `og:image` adreslerini ve `robots.txt` + `sitemap.xml` URL'lerini güncelleyin (head'de `NOT:` yorumuyla işaretli).

## İş takibi

Çalışmalar epic + sub-issue düzeninde yürür: [Epic #1](https://github.com/vtknightmare/apikultur-vakfi/issues/1).
