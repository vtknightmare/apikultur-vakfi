# Apikültür Vakfı — Web Sitesi

Apikültür Vakfı'nın resmî web sitesi. **Doğayı Geleceğe Taşır.**

Canlı adres (geçici): **https://vtknightmare.github.io/apikultur-vakfi/**
(apikulturvakfi.com bağlandığında güncellenecek)

## Yapı

Tek dosyalık statik bir site — derleme adımı, framework ya da bağımlılık yok.

| Dosya | İçerik |
|---|---|
| `index.html` | Sitenin tamamı: içerik, stil (inline CSS), davranış (vanilla JS), TR/EN çeviri sözlükleri |
| `assets/` | favicon, apple-touch-icon, sosyal paylaşım görseli (og-image) |
| `robots.txt`, `sitemap.xml` | Arama motoru dosyaları |

İçerik kaynağı: `Apikultur_Vakfi_Site_Metni.docx` (final taslak, Alican).

## Güncelleme

1. `index.html` içinde ilgili metni düzenleyin. **Dikkat:** Görünen metinlerin çoğu sayfa gövdesinde *ve* `<script>` içindeki `I18N` sözlüğünde (TR + EN) yer alır — ikisini de güncelleyin, yoksa dil değiştirildiğinde eski metin geri gelir.
2. `main` dalına commit + push yapın. GitHub Pages otomatik olarak yeniden yayınlar (1-2 dk).

## Alan adı bağlanacağı zaman

1. Repo → Settings → Pages → Custom domain: `apikulturvakfi.com` (CNAME dosyası otomatik oluşur)
2. DNS: `A` kayıtları → GitHub Pages IP'leri, `www` → CNAME `vtknightmare.github.io`
3. `index.html` içindeki canonical / `og:url` / `og:image` adreslerini ve `robots.txt` + `sitemap.xml` URL'lerini güncelleyin (head'de `NOT:` yorumuyla işaretli).

## İş takibi

Çalışmalar epic + sub-issue düzeninde yürür: [Epic #1](https://github.com/vtknightmare/apikultur-vakfi/issues/1).
