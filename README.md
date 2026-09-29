# Sendikacılık Akademisi Ders Notları 1–4

TÜRK-İŞ’in *Sendikacılık Akademisi Ders Notları* dizisinin (4 cilt) çevrim içi okuma ve arama aracı. Metinler, her cildin **içindekiler** sayfasına göre bölümlere ayrılmış ve konu alanlarına göre sınıflandırılmıştır.

| Cilt | Yıl | Yürütücü üniversite | Bölüm |
|---|---|---|---|
| Ders Notları 1 | 2012 | İstanbul Aydın Üniversitesi | 16 |
| Ders Notları 2 | 2013 | Ankara Üniversitesi SBF | 19 |
| Ders Notları 3 | 2013 | İstanbul Aydın Üniversitesi | 10 |
| Ders Notları 4 | 2016 | Uludağ Üniversitesi ÇEEİ | 20 |

**Toplam:** 65 bölüm · 45 yazar · 2.109 sayfa · ~614 bin kelime

## Özellikler

- **Üç gezinme görünümü:** Kitap (içindekiler sırası) · Konu alanı (11 alan) · Yazar
- **Tam metin arama:** tüm ciltlerde ya da tek ciltte; sonuçlar bölüm ve sayfa numarasıyla, tıklayınca ilgili sayfada vurgulu açılır
- **Bölüm içi arama**, sayfa numarasına atlama, yazı boyutu, TXT indirme ve kopyalama
- Her bölümün paylaşılabilir bağlantısı vardır (ör. `#k2-4` → DN 2, Türkiye Çalışma İlişkileri Tarihi)
- Açık/koyu tema, mobil uyumlu; sunucu tarafı kod ya da derleme adımı gerektirmez

## Dosya yapısı

```
index.html        Arayüz (HTML + CSS + JS, tek dosya)
data/dn1.js …     Cilt başına metin verisi (bölüm → [sayfa no, metin])
favicon.svg
.nojekyll         GitHub Pages'in Jekyll işlemesini kapatır
```

Veri biçimi: `{ n, title, meta, ch: [ { a: yazar, t: başlık, s: başlangıç sayfası, th: konu alanı, p: [[sayfa, metin], …] } ] }`. Metinde paragraflar `\n\n` ile ayrılır.

## GitHub Pages’te yayınlama

1. GitHub’da yeni bir depo açın (ör. `sendikacilik-akademisi`).
2. Bu klasörün **içeriğini** depo köküne yükleyin (*Add file → Upload files* ya da `git push`).
3. *Settings → Pages → Build and deployment → Source: Deploy from a branch*, dal: `main`, klasör: `/ (root)` → **Save**.
4. Birkaç dakika sonra site `https://<kullanıcı-adı>.github.io/sendikacilik-akademisi/` adresinde yayında olur.

Yerelde denemek için `index.html` dosyasını doğrudan tarayıcıda açmanız yeterlidir.

## Metin işleme notları

Metinler OCR/PDF metin çıkarımından gelmektedir ve otomatik olarak temizlenmiştir: satır sonu tirelemeleri birleştirilmiş, sabit satır kırılımları paragraflara dönüştürülmüş, bozuk dipnot ayırıcıları kaldırılıp dipnotlar `[n]` biçiminde ayrılmış, sembol fontu karakterleri madde işaretlerine çevrilmiştir. Paragraf ayrımı sezgiseldir; tablolar düz metne dönüşmüş olabilir. Alıntılarda basılı sayfa numaralarını (s.) esas alınız.

*Konu alanı sınıflandırması derleyiciye aittir, özgün yayında yer almaz.*

## Kaynak ve haklar

*Sendikacılık Akademisi Ders Notları* 1–4. Türkiye İşçi Sendikaları Konfederasyonu (TÜRK-İŞ), Ankara, 2012–2016. Metinlerin tüm hakları yazarlarına ve TÜRK-İŞ’e aittir; bu depo yalnızca erişim ve arama kolaylığı amacıyla hazırlanmıştır.
