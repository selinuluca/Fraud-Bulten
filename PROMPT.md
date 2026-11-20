# Proje promptu

Bu projeyi başka bir Claude hesabında veya bilgisayarda aynı şekilde sürdürmek için aşağıdaki metni olduğu gibi yapıştırın.

```
# Proje: Fraud & Teknoloji Bülteni

Her hafta dünyadan ve Türkiye'den en önemli 10 haberi (dijital fraud/dolandırıcılık, önemli siber güvenlik, yeni teknoloji/AI) seçip Türkçe özetleyen ve GitHub Pages'te yayımlayan bir sistem yürütüyoruz. Tarama, seçim ve özetleme işini sen yapıyorsun. API anahtarı, Python botu ve Telegram yok.

## Mevcut durum
- Repo: github.com/selinuluca/Fraud-Bulten (public). Site: https://selinuluca.github.io/Fraud-Bulten/ (Pages: main dalı, /root).
- Repodaki dosyalar: index.html (tek sayfa, derleme yok), data/index.json (hafta listesi, en yenisi en üstte), data/YYYY-AA-GG.json (haftanın 10 haberi), EDITORYAL.md (yayın ilkeleri), kaynaklar.md (kaynaklar, ölçütler, kota), README.md.
- İlk sayı (16 Kasım 2026) yayında ve onaylı. Ona dokunma, ama örnek de alma: o sayı uzunluk kuralından önce yazıldı.
- İlk iş: repoyu push erişimiyle bağla, klonla ve dosyaları oku. Eksik dosya varsa bu prompttaki kurallara göre oluştur.

## Haftalık iş (her Pazartesi akşamı)
1. EDITORYAL.md, kaynaklar.md ve README.md'yi oku ve uygula. Bu promptla çelişirlerse dosyalar geçerlidir, çünkü onları ben güncelliyorum.
2. Son 4 haftanın dosyalarını kontrol et: aynı URL'yi veya aynı olayı tekrar alma.
3. Son 7 günü tara. Türkiye ve dünya için ayrı ayrı, hem Türkçe hem İngilizce arama yap; kaynaklar.md'deki listeye de bak. X/Twitter yalnızca ipucu olarak kullanılır; her haber güvenilir bir kaynaktan doğrulanır.
4. Aday haberleri gerçekten açıp oku. Açılmayan veya doğrulanamayan haberi ya da bağlantıyı kullanma. Mümkünse birincil kaynağı (resmî duyuruyu) bağla.
5. Tam 10 haber seç. Esnek kota: yaklaşık 4 fraud, 3 siber, 3 AI/teknoloji; en az 2-3 Türkiye haberi.
6. data/YYYY-AA-GG.json dosyasını oluştur ve data/index.json listesinin başına ekle; başka hiçbir dosyaya dokunma. Kontrol et: JSON geçerli mi, tam 10 haber var mı, uzunluk sınırı aşılmış mı, bağlantılar açılıyor mu, önceki haftalarla tekrar var mı. Sonra main dalına commit ve push yap ("Haftalık sayı: <label>").
7. Bana kısa bir Türkçe rapor yaz: 10 başlık sırasıyla, kategori ve Türkiye/dünya dağılımı, doğrulayamadığın için dışarıda bıraktığın önemli haberler. Bir sorun olduysa raporun en başında söyle.

## Veri biçimi
{"date":"2026-11-23","label":"17–23 Kasım 2026","items":[{"title":"","summary":"","category":"fraud|siber|ai","region":"tr|dunya","source":"","url":"","date":"YYYY-AA-GG","more":[{"source":"","url":""}]}]}
(more isteğe bağlı, ikinci kaynak için)

## Yayın ilkeleri (okuyucu: bankacılık ve ödeme tarafında fraud ile ilgilenen biri)
- Sıralama: en üste ödeme ve fraud dünyasını değiştiren yeni teknolojiler (ajanların yaptığı ödemeler, yeni ödeme yöntemleri, yapay zekâ destekli fraud); ardından yeni dolandırıcılık ve saldırı yöntemleri; sonra siber güvenlik olayları; en sonda rutin veri ihlali duyuruları.
- Uzunluk: en fazla 4 satır, yani en fazla 4 kısa cümle ve yaklaşık 400 karakter. Virgüllerle uzayan cümle kurma; sığmayan ayrıntıyı at.
- Odak: "kim, kaç kişi, kaç para" değil; "nasıl yapılıyor, nasıl tespit edildi, kullanıcı ve banka neye dikkat etmeli". Gözaltı ve tutuklama sayıları, el konulan altyapı, açıkta kalan sunucu sayısı gibi yan bilgileri yazma.
- Terimleri ilk geçtikleri yerde kısaca açıkla (ör. "onay oltalaması").
- Yeni ödeme sistemi veya teknoloji haberlerinde nasıl çalıştığını ve geleneksel yöntemden farkını anlat.
- Güvenlik açıklarını "şöyle bir zafiyet vardı, şuna yol açıyordu, üretici kapattı" diye anlat ve bankacılık açısından anlamını ekle.
- Model ve ürün sürümlerinde fiyat yerine önceki sürüme göre neyin değiştiğini yaz.
- Rutin veri ihlali duyurularına (ör. KVKK bildirimleri) en fazla 1-2 cümle ayır.
- Büyük altyapı kesintileri de haber adayıdır (ör. Microsoft 365 kesintisi).
- Metni kaynaktan kopyalama, kendi cümlelerinle yaz; kaynakta olmayan bilgiyi ekleme.

## Kaynaklar (başlangıç listesi)
- TR: KVKK veri ihlali bildirimleri, USOM, Siber Güvenlik Başkanlığı, BTK, BDDK, TCMB, MASAK, SPK, İçişleri/Emniyet açıklamaları (AA, DHA), BKM, ShiftDelete, Webrazzi.
- Fraud ve ödeme: Finextra, The Paypers, PYMNTS, Merchant Risk Council, ABD Adalet Bakanlığı, FBI/IC3, Europol, FCA/PSR, ECB/EBA, FTC.
- Siber: BleepingComputer, The Record, KrebsOnSecurity, Dark Reading, SecurityWeek, The Hacker News, CISA KEV.
- AI: OpenAI, Anthropic, Google, Microsoft ve Meta'nın kendi duyuruları; Visa, Mastercard; TechCrunch, Reuters.
- Banka basın bülteni sayfalarını kullanma: gürültü üretiyorlar.

## Site (index.html yeniden yazılması gerekirse)
Başlık "Fraud & Teknoloji Bülteni", hafta seçici, filtreler (Tümü / Fraud / Siber güvenlik / AI-Teknoloji / Türkiye). Haberler numaralı listelenir; her haberde kategori, bölge, başlık, özet, tarih ve kaynak bağlantısı bulunur. Üstte slogan veya "haftanın teması" cümlesi olmasın. Altta yalnızca şu not: haftalık güncellenir, özetler Claude tarafından yazılır, doğrulama için kaynağa bakılmalıdır. Açık/koyu tema desteklensin.

## Kurulum
Repoyu bağladıktan sonra her Pazartesi 18:45 civarında (Europe/Istanbul) çalışan bir zamanlanmış görev oluştur. Görev yukarıdaki "Haftalık iş" adımlarını soru sormadan yapsın ve bitince bana bildirim göndersin.
```

Not: Bu repoya yazan haftalık görev şu an başka bir Claude hesabında çalışıyor (her Pazartesi 18:43). Yeni bir hesapta da aynı repoya yazan bir görev kurulursa haftalık sayı iki kez oluşur; ikisinden yalnızca biri çalışmalı.
