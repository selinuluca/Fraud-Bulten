# Proje promptu

Bu bülten sistemini kendi Claude hesabınızda kurmak için aşağıdaki metni Claude'a olduğu gibi yapıştırın. Haberler her hafta Claude'da hazırlanır ve size bildirim gelir; GitHub Pages'te yayımlamak isteğe bağlıdır.

```
# Proje: Fraud & Teknoloji Bülteni

Her hafta dünyadan ve Türkiye'den öne çıkan dijital fraud, bankacılığın geleceği ve ödeme teknolojileri, önemli siber güvenlik ve yeni teknoloji/AI haberlerini seçip Türkçe özetleyen bir bülten istiyorum. Tarama, seçim ve özetleme işini sen yapacaksın.

## Kurulum
1. Hemen son 7 günden ilk sayıyı "Haftalık iş" adımlarına göre hazırla ve bana bu sohbette göster.
2. İlk sayıyı onaylarsam (veya düzeltmelerimi uyguladıktan sonra) her Pazartesi 19:00 civarında (Europe/Istanbul) çalışan bir zamanlanmış görev kur ve bitince bana bildirim gönderilsin. Görevin talimatı bu promptun "Haftalık iş", "Yayın ilkeleri", "Kaynaklar ve ölçütler" ve "Rapor biçimi" bölümlerinin tamamını içersin; görev her seferinde sıfırdan başlar, başka bir dosyaya veya bu sohbete bakamaz.
3. En sonda bana bülteni ayrıca bir web sayfası olarak (GitHub Pages) yayımlamak isteyip istemediğimi sor. İstemezsem bülten yalnızca Claude'da kalır. İstersem "GitHub Pages (isteğe bağlı)" bölümünü uygula.

## Haftalık iş
1. Bugünün tarihini al. Son 7 günün (bugün dahil) haberlerini tara. Türkiye ve dünya için ayrı ayrı, hem Türkçe hem İngilizce web araması yap; aşağıdaki kaynak listesine de bak. Tarih aralığı dışındaki haberleri alma.
2. Aday haberleri gerçekten açıp oku. Açılmayan veya doğrulanamayan haberi ya da bağlantıyı kullanma; tek kaynaklı iddiaları alma. Mümkünse birincil kaynağı (resmî duyuruyu) bağla. X/Twitter yalnızca ipucudur.
3. Okurken kaynak haberin ana metninin yaklaşık kelime sayısını not et (okuma süresi için) ve aynı olayı kendi haberi olarak veren kaç farklı saygın yayın bulduğunu say (gündem etkisi).
4. Haber sayısı sabit değil: aşağıdaki ölçütleri geçen her haber girer, önem sırasına göre dizilir. Dolgu haber koyma.
5. GitHub Pages kurulduysa repodaki son 4 haftanın dosyalarına bak ve aynı olayı tekrar alma; kurulmadıysa yalnızca son 7 günle sınırlı kal.
6. Raporu aşağıdaki "Rapor biçimi"ne göre yaz. GitHub Pages kurulduysa ayrıca sayıyı repoya ekle (o bölümdeki adımlar).

## Yayın ilkeleri (okuyucu: bankacılık ve ödeme tarafında fraud ile ilgilenen biri)
- Öncelikli konu, bankacılığın geleceği. Bu haberlere daha çok yer ver: yeni bankacılık kanalları, yeni ödeme sistemleri ve yöntemleri, bankacılık teknolojisi, fraud önleme çözümleri. Türkiye'deki karşılıklarını özellikle ara.
- Sıralama: en üste bankacılığın ve ödemenin geleceğini değiştiren gelişmeler (ajanların yaptığı ödemeler, yeni ödeme sistemleri ve kanallar, yapay zekâ destekli fraud, yeni fraud önleme teknolojileri); ardından yeni dolandırıcılık ve saldırı yöntemleri; sonra siber güvenlik olayları; en sonda rutin veri ihlali duyuruları. Gündem etkisi yardımcı ölçüttür, bu sıranın önüne geçmez.
- Uzunluk: en fazla 4 satır, yani en fazla 4 kısa cümle ve yaklaşık 400 karakter. Virgüllerle uzayan cümle kurma; sığmayan ayrıntıyı at.
- Odak: "kim, kaç kişi, kaç para" değil; "nasıl yapılıyor, nasıl tespit edildi, kullanıcı ve banka neye dikkat etmeli". Gözaltı ve tutuklama sayıları, el konulan altyapı, açıkta kalan sunucu sayısı gibi yan bilgileri yazma.
- Terimleri ilk geçtikleri yerde kısaca açıkla (ör. "onay oltalaması").
- Yeni ödeme sistemi veya teknoloji haberlerinde nasıl çalıştığını ve geleneksel yöntemden farkını anlat.
- Güvenlik açıklarını "şöyle bir zafiyet vardı, şuna yol açıyordu, üretici kapattı" diye anlat ve bankacılık açısından anlamını ekle.
- Model ve ürün sürümlerinde fiyat yerine önceki sürüme göre neyin değiştiğini yaz.
- Rutin veri ihlali duyurularına (ör. KVKK bildirimleri) en fazla 1-2 cümle ayır.
- Büyük altyapı kesintileri de haber adayıdır (ör. Microsoft 365 kesintisi).
- Okuma süresi: kaynak haberin kelime sayısı / 220, yukarı yuvarla. Yayıncı süreyi kendisi veriyorsa onu kullan. Bilinmiyorsa yazma.
- Gündem etkisi: kaynak sitelerin tıklanma sayıları dışarıdan görülemez; bunun yerine haberin kaç farklı saygın yayında kendi haberi olarak yer aldığını say (kopya, toplayıcı ve tarama siteleri hariç). Emin değilsen yazma, şişirme.
- Metni kaynaktan kopyalama, kendi cümlelerinle yaz; kaynakta olmayan bilgiyi ekleme.

## Kaynaklar ve ölçütler (başlangıç listesi; aramayla bulunan başka güvenilir kaynaklar da kullanılır)
- Bankacılığın geleceği: TCMB ödeme sistemleri (FAST, TR Karekod), BKM, TBB; Türk bankalarının yeni kanal, ödeme ve fraud önleme ürünü duyuruları (ödül, sponsorluk, finansal sonuç haberleri hariç); Finextra, The Financial Brand, Payments Dive, American Banker, Webrazzi Fintech; Visa ve Mastercard inovasyon duyuruları; wero, Pix, UPI gibi yeni ödeme sistemleri.
- Türkiye: KVKK veri ihlali bildirimleri, USOM, Siber Güvenlik Başkanlığı, BTK, BDDK, MASAK, SPK, İçişleri/Emniyet açıklamaları (AA, DHA), ShiftDelete, Webrazzi.
- Fraud ve ödeme: Finextra, The Paypers, PYMNTS, Merchant Risk Council, ABD Adalet Bakanlığı, FBI/IC3, Europol, FCA/PSR, ECB/EBA, FTC.
- Siber: BleepingComputer, The Record, KrebsOnSecurity, Dark Reading, SecurityWeek, The Hacker News, CISA KEV.
- AI: OpenAI, Anthropic, Google, Microsoft ve Meta'nın kendi duyuruları; TechCrunch, Reuters.
- Seçim ölçütleri: etki (kaç kişi/kurum, ne kadar yaygın), yenilik (yeni yöntem, düzenleme, teknoloji), Türkiye ve bankacılık açısından ilgililik, güvenilirlik (birincil kaynak veya saygın yayın). Türkiye haberleri her hafta aranır (tercihen en az 2-3).

## Rapor biçimi (Claude'da gösterilen haftalık bülten)
- Başlık: "Fraud & Teknoloji Bülteni — <tarih aralığı>" ve altında tek satır: "N haber · özetlerin tamamı yaklaşık X dk".
- Haberler önem sırasına göre numaralı. Her haber için:
  - **Başlık** (kalın)
  - Etiket satırı: kategori (Fraud / Siber güvenlik / AI-Teknoloji) · bölge (Türkiye / Dünya)
  - Özet (en fazla 4 kısa cümle)
  - Bilgi satırı: "⏱ Kaynak haber: X dk okuma · 📰 Y farklı yayında yer aldı" (bilinmeyen kısmı yazma)
  - Tarih ve tıklanabilir kaynak bağlantısı
- Sonda kısa not: doğrulayamadığın için dışarıda bıraktığın önemli haberler. Bir sorun olduysa (yeterli haber bulunamadı, kaynaklar açılmadı) bunu raporun en başında söyle.

## GitHub Pages (isteğe bağlı, yalnızca istersem)
1. Benden kendi GitHub hesabımda açtığım repo bağlantısını iste. Repo public olmalı (ücretsiz planda Pages yalnızca public repoda çalışır). Başka bir repoya yazma.
2. Repoyu push erişimiyle bağla. Bağlanamazsan GitHub'ı Claude'a nasıl bağlayacağımı (Customize → Connectors → GitHub; gerekirse Claude GitHub uygulamasını repoya kurma) adım adım anlat.
3. Repoda şunları oluştur: index.html (site), data/index.json, o haftanın data/YYYY-AA-GG.json dosyası, README.md (yapı ve veri biçimi). Sonra bana Pages'i nasıl açacağımı anlat: Settings → Pages → Deploy from a branch → main / (root) → Save. Site adresi: https://<kullanıcı>.github.io/<repo>/
4. Zamanlanmış görevin talimatına şunu ekle: her hafta raporu yazdıktan sonra data/YYYY-AA-GG.json dosyasını oluştur, data/index.json listesinin başına ekle, başka dosyaya dokunma, JSON'u doğrula, main dalına commit ve push yap ("Haftalık sayı: <tarih aralığı>"), rapora site adresini ekle.
5. Veri biçimi:
   data/index.json: {"issues":[{"date":"2026-11-23","file":"2026-11-23.json","label":"17–23 Kasım 2026"}]}  (en yenisi en üstte)
   Haftalık dosya: {"date":"2026-11-23","label":"17–23 Kasım 2026","items":[{"title":"","summary":"","category":"fraud|siber|ai","region":"tr|dunya","source":"","url":"","read_min":4,"coverage":12,"date":"YYYY-AA-GG","more":[{"source":"","url":""}]}]}  (read_min, coverage ve more isteğe bağlı)
6. Site (index.html):
   - Tek dosya, derleme adımı yok; data/index.json ve haftalık dosyaları fetch ile okur. İçerik textContent ile yazılır (innerHTML yok). Açık/koyu tema desteklenir.
   - Üstte yalnızca "Fraud & Teknoloji Bülteni" başlığı; slogan veya "haftanın teması" cümlesi yok. Altında hafta seçici ve filtreler: Tümü / Fraud / Siber güvenlik / AI-Teknoloji / Türkiye / Okunmamış.
   - Listenin üstünde: "N haber · M okunmamış · özetlerin tamamı yaklaşık X dk".
   - Haberler numaralı. Her haberde kategori ve bölge etiketi, başlık, özet; altında varsa "⏱ Kaynak haber: X dk okuma · 📰 Y farklı yayında yer aldı" etiketi; onun altında tarih, kaynak bağlantısı ve "Okundu işaretle" düğmesi.
   - Okundu takibi: kaynak bağlantısına tıklanan ya da düğmeyle işaretlenen haber soluklaşır, numarasının altına ✓ gelir (düğmeyle geri alınır). Ziyaret edilmiş bağlantılar mor görünür. Bilgi localStorage'da tutulur (try/catch ile) ve yalnızca o tarayıcıda geçerlidir.
   - Altta yalnızca şu not: haftalık güncellenir, özetler Claude tarafından yazılır, doğrulama için kaynağa bakılmalıdır.
```
