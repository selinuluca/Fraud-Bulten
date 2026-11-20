# Proje promptu

Bu bülten sistemini kendi GitHub hesabınızda kurup sürdürmek için aşağıdaki metni Claude'a olduğu gibi yapıştırın. Claude sizden kendi repo bağlantınızı isteyecek ve her şeyi o repoya kuracak.

```
# Proje: Fraud & Teknoloji Bülteni

Her hafta dünyadan ve Türkiye'den öne çıkan dijital fraud, bankacılığın geleceği ve ödeme teknolojileri, önemli siber güvenlik ve yeni teknoloji/AI haberlerini seçip Türkçe özetleyen ve GitHub Pages'te yayımlayan bir sistem kuracağız. Tarama, seçim ve özetleme işini sen yapacaksın. API anahtarı, Python botu ve Telegram yok.

## Kurulum
1. Benden kendi GitHub hesabımda açtığım repo bağlantısını iste. Repo public olmalı (ücretsiz planda Pages yalnızca public repoda çalışır). Bağlantıyı vermeden başlama; başka bir repoya yazma.
2. Repoyu push erişimiyle bağla. Bağlanamazsan GitHub'ı Claude'a nasıl bağlayacağımı (Customize → Connectors → GitHub, gerekirse Claude GitHub uygulamasını repoya kurma) adım adım anlat.
3. Repoda şu dosyaları oluştur: index.html (site), data/index.json, EDITORYAL.md (aşağıdaki yayın ilkeleri), kaynaklar.md (aşağıdaki kaynaklar ve ölçütler), README.md (yapı, veri biçimi, Pages ve sayaç kurulumu).
4. Son 7 günden ilk sayıyı hazırla, gönder, sonra bana Pages'i nasıl açacağımı anlat: Settings → Pages → Deploy from a branch → main / (root) → Save. Site adresi: https://<kullanıcı>.github.io/<repo>/
5. İlk sayıyı onaylarsam her Pazartesi 18:45 civarında (Europe/Istanbul) çalışan bir zamanlanmış görev kur. Görev "Haftalık iş" adımlarını soru sormadan yapsın ve bitince bana bildirim göndersin.

## Haftalık iş (her Pazartesi akşamı)
1. EDITORYAL.md, kaynaklar.md ve README.md'yi oku ve uygula. Bu promptla çelişirlerse dosyalar geçerlidir, çünkü onları ben güncelliyorum.
2. Son 4 haftanın dosyalarını kontrol et: aynı URL'yi veya aynı olayı tekrar alma.
3. Son 7 günü tara. Türkiye ve dünya için ayrı ayrı, hem Türkçe hem İngilizce arama yap; kaynaklar.md'deki listeye de bak. X/Twitter yalnızca ipucu olarak kullanılır; her haber güvenilir bir kaynaktan doğrulanır.
4. Aday haberleri gerçekten açıp oku. Açılmayan veya doğrulanamayan haberi ya da bağlantıyı kullanma. Mümkünse birincil kaynağı (resmî duyuruyu) bağla.
5. Haber sayısı sabit değil: ölçütleri geçen her haber girer, önem sırasına göre dizilir. Dolgu haber koyma.
6. data/YYYY-AA-GG.json dosyasını oluştur ve data/index.json listesinin başına ekle; başka hiçbir dosyaya dokunma. Kontrol et: JSON geçerli mi, uzunluk sınırı aşılmış mı, bağlantılar açılıyor mu, önceki haftalarla tekrar var mı. Sonra main dalına commit ve push yap ("Haftalık sayı: <label>").
7. Bana kısa bir Türkçe rapor yaz: başlıklar sırasıyla, haber sayısı, kategori ve Türkiye/dünya dağılımı, doğrulayamadığın için dışarıda bıraktığın önemli haberler. Bir sorun olduysa raporun en başında söyle.

## Veri biçimi
data/index.json: {"issues":[{"date":"2026-11-23","file":"2026-11-23.json","label":"17–23 Kasım 2026"}]}  (en yenisi en üstte)
Haftalık dosya: {"date":"2026-11-23","label":"17–23 Kasım 2026","items":[{"title":"","summary":"","category":"fraud|siber|ai","region":"tr|dunya","source":"","url":"","read_min":4,"date":"YYYY-AA-GG","more":[{"source":"","url":""}]}]}
(read_min ve more isteğe bağlı)

## Yayın ilkeleri (okuyucu: bankacılık ve ödeme tarafında fraud ile ilgilenen biri)
- Öncelikli konu, bankacılığın geleceği. Bu haberlere daha çok yer ver: yeni bankacılık kanalları, yeni ödeme sistemleri ve yöntemleri, bankacılık teknolojisi, fraud önleme çözümleri. Türkiye'deki karşılıklarını özellikle ara.
- Sıralama: en üste bankacılığın ve ödemenin geleceğini değiştiren gelişmeler (ajanların yaptığı ödemeler, yeni ödeme sistemleri ve kanallar, yapay zekâ destekli fraud, yeni fraud önleme teknolojileri); ardından yeni dolandırıcılık ve saldırı yöntemleri; sonra siber güvenlik olayları; en sonda rutin veri ihlali duyuruları.
- Uzunluk: en fazla 4 satır, yani en fazla 4 kısa cümle ve yaklaşık 400 karakter. Virgüllerle uzayan cümle kurma; sığmayan ayrıntıyı at.
- Odak: "kim, kaç kişi, kaç para" değil; "nasıl yapılıyor, nasıl tespit edildi, kullanıcı ve banka neye dikkat etmeli". Gözaltı ve tutuklama sayıları, el konulan altyapı, açıkta kalan sunucu sayısı gibi yan bilgileri yazma.
- Terimleri ilk geçtikleri yerde kısaca açıkla (ör. "onay oltalaması").
- Yeni ödeme sistemi veya teknoloji haberlerinde nasıl çalıştığını ve geleneksel yöntemden farkını anlat.
- Güvenlik açıklarını "şöyle bir zafiyet vardı, şuna yol açıyordu, üretici kapattı" diye anlat ve bankacılık açısından anlamını ekle.
- Model ve ürün sürümlerinde fiyat yerine önceki sürüme göre neyin değiştiğini yaz.
- Rutin veri ihlali duyurularına (ör. KVKK bildirimleri) en fazla 1-2 cümle ayır.
- Büyük altyapı kesintileri de haber adayıdır (ör. Microsoft 365 kesintisi).
- Okuma süresi: read_min alanına kaynak haberin tahmini okuma süresini yaz (ana metnin kelime sayısı / 220, yukarı yuvarla). Yayıncı süreyi kendisi veriyorsa onu kullan; belirleyemiyorsan alanı boş bırak.
- Metni kaynaktan kopyalama, kendi cümlelerinle yaz; kaynakta olmayan bilgiyi ekleme.

## Kaynaklar ve ölçütler (başlangıç listesi)
- Bankacılığın geleceği: TCMB ödeme sistemleri (FAST, TR Karekod), BKM, TBB; Türk bankalarının yeni kanal, ödeme ve fraud önleme ürünü duyuruları (ödül, sponsorluk, finansal sonuç haberleri hariç); Finextra, The Financial Brand, Payments Dive, American Banker, Webrazzi Fintech; Visa ve Mastercard inovasyon duyuruları; wero, Pix, UPI gibi yeni ödeme sistemleri.
- TR: KVKK veri ihlali bildirimleri, USOM, Siber Güvenlik Başkanlığı, BTK, BDDK, MASAK, SPK, İçişleri/Emniyet açıklamaları (AA, DHA), ShiftDelete, Webrazzi.
- Fraud ve ödeme: Finextra, The Paypers, PYMNTS, Merchant Risk Council, ABD Adalet Bakanlığı, FBI/IC3, Europol, FCA/PSR, ECB/EBA, FTC.
- Siber: BleepingComputer, The Record, KrebsOnSecurity, Dark Reading, SecurityWeek, The Hacker News, CISA KEV.
- AI: OpenAI, Anthropic, Google, Microsoft ve Meta'nın kendi duyuruları; TechCrunch, Reuters.
- Seçim ölçütleri: etki (kaç kişi/kurum, ne kadar yaygın), yenilik (yeni yöntem, düzenleme, teknoloji), Türkiye ve bankacılık açısından ilgililik, güvenilirlik (birincil kaynak veya saygın yayın; tek kaynaklı iddia yok). Türkiye haberleri her hafta aranır (tercihen en az 2-3).

## Site (index.html)
- Tek dosya, derleme adımı yok; data/index.json ve haftalık dosyaları fetch ile okur.
- Üstte yalnızca "Fraud & Teknoloji Bülteni" başlığı; slogan veya "haftanın teması" cümlesi yok. Altında hafta seçici ve filtreler (Tümü / Fraud / Siber güvenlik / AI-Teknoloji / Türkiye).
- Listenin üstünde: "N haber · özetlerin tamamı yaklaşık X dk" (başlık + özet kelime sayısı / 180).
- Haberler numaralı listelenir. Her haberde kategori ve bölge etiketi, başlık ve özet bulunur. Özetin altında, read_min varsa "⏱ Kaynak haber: X dk okuma" etiketi; onun altında tarih ve kaynak bağlantısı.
- Altta yalnızca şu not: haftalık güncellenir, özetler Claude tarafından yazılır, doğrulama için kaynağa bakılmalıdır. Açık/koyu tema desteklensin. İçerik textContent ile yazılsın (innerHTML yok).
- İsteğe bağlı sayaç (GoatCounter, çerezsiz): index.html'de `const GOATCOUNTER = ""` ayarı olsun. Kod yazılınca sayfa görüntülenmeleri ve her haberin kaynak bağlantısına tıklamalar ("tik/<tarih>/<sıra>" olayı) sayılır. GoatCounter'da "Allow adding visitor counts on your website" açıksa sayılar sayfada da görünür ("sayfa X kez görüntülendi", haber altında "X tıklama"). Kod boşsa sayaç tamamen kapalı. Hesabı ben açarım, kodu sana veririm.
```
