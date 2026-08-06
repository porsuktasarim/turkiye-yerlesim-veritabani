# Türkiye Yerleşim Birimleri

Türkiye'nin il, ilçe, mahalle ve köy verilerini geliştiriciler için düzenlenmiş, kullanımı kolay JSON ve XML formatlarında sunmayı amaçlayan açık kaynak veri seti.

> ⚠️ Proje henüz geliştirme aşamasındadır. Şu anda il ve ilçe dosya yapısı yeniden düzenlenmiştir. Mahalle ve köy verilerinin düzenlenmesi devam etmektedir.

## Amaç

Bu proje, mevcut Türkiye yerleşim verilerini daha düzenli, okunabilir ve geliştirici dostu bir yapıya dönüştürmeyi amaçlamaktadır.

Başlıca hedefler:

- İl bazında tek dosya desteği
- İlçe bazında ayrı dosya desteği
- Tüm Türkiye verisinin tek dosyada sunulması
- JSON ve XML formatlarının birlikte sağlanması
- Standart dosya adlandırması
- Temizlenmiş yerleşim adları
- Açık kaynak ve kolay kullanılabilir veri yapısı

## Dosya Yapısı

```text
data/
└── turkey/
    │
    ├── turkey.json
    ├── turkey.xml
    │
    ├── 34-istanbul.json
    ├── 34-istanbul.xml
    ├── 34-istanbul/
    │   ├── 01-adalar.json
    │   ├── 01-adalar.xml
    │   ├── ...
    │   ├── 39-silivri.json
    │   └── 39-silivri.xml
    │
    └── ...
```

## Dosya Adlandırma Kuralları

- Dosya adları küçük harftir.
- Türkçe karakter kullanılmaz.
- İl dosyaları plaka kodu ile başlar.

Örnek:

```
34-istanbul.json
06-ankara.json
35-izmir.json
```

İlçe dosyaları il içerisindeki sıra numarası ile başlar.

Örnek:

```
01-adalar.json
02-arnavutkoy.json
39-silivri.json
```

Eğer ilde **Merkez** ilçesi bulunuyorsa her zaman ilk sırada yer alır.

Örnek:

```
01-merkez.json
02-agacoren.json
03-eskil.json
```

## Veri Kaynağı

Bu proje aşağıdaki açık kaynak çalışmayı temel almaktadır:

https://github.com/nejdetkadir/il-ilce-semt-mahalleler

Veriler yeniden düzenlenmiş, dosya yapısı standartlaştırılmış ve geliştirici dostu hale getirilmektedir.

## Yol Haritası

- [x] İl klasör yapısı
- [x] İl JSON dosyaları
- [x] İl XML dosyaları
- [x] İlçe JSON dosyaları
- [x] İlçe XML dosyaları
- [ ] Mahalle adlarının düzenlenmesi
- [ ] Köy adlarının düzenlenmesi
- [ ] Gereksiz "Mah.", "Mahallesi", "Köy", "Köyü" eklerinin temizlenmesi
- [ ] Sürüm numaralandırması
- [ ] Otomatik üretim betiği

## Lisans

Kaynak verinin lisansına uygun olarak kullanılmaktadır.
