# Fraud & Teknoloji Bülteni

Dünyadan ve Türkiye'den haftanın öne çıkan fraud, bankacılık ve ödeme teknolojisi, siber güvenlik ve AI haberleri (sayı her hafta değişir, önem sırasına göre). Her haber en fazla dört satırda Türkçe özetlenir. Her Pazartesi akşamı güncellenir.

## Yapı

- `index.html`: site. En son haftayı gösterir, geçmiş haftalar açılır listeden seçilir. Derleme adımı yoktur.
- `data/index.json`: hafta listesi, en yenisi en üstte.
- `data/YYYY-AA-GG.json`: o haftanın haberleri (yayın tarihiyle adlandırılır).
- `kaynaklar.md`: taranan kaynaklar ve seçim ölçütleri.
- `EDITORYAL.md`: haber seçimi ve özet yazımı için yayın ilkeleri.
- `PROMPT.md`: projeyi başka bir Claude hesabında sürdürmek için tam prompt.

## Haftalık dosya biçimi

```json
{
  "date": "2026-11-16",
  "label": "9–16 Kasım 2026",
  "items": [
    {
      "title": "Türkçe başlık",
      "summary": "En fazla 4 kısa cümle, yaklaşık 400 karakter.",
      "category": "fraud | siber | ai",
      "region": "tr | dunya",
      "source": "Kaynak adı",
      "url": "https://...",
      "read_min": 4,
      "coverage": 12,
      "more": [{ "source": "İkinci kaynak (isteğe bağlı)", "url": "https://..." }],
      "date": "2026-11-13"
    }
  ]
}
```

`read_min` kaynak haberin tahmini okuma süresidir (dakika). `coverage` haberin kaç farklı yayında yer aldığıdır (gündem etkisi). İkisi de isteğe bağlıdır.

Okundu bilgisi: kaynak bağlantısına tıklanan veya "Okundu işaretle" ile işaretlenen haberler soluklaşır ve ✓ alır; "Okunmamış" filtresi yalnızca kalanları gösterir. Bilgi okuyucunun kendi tarayıcısında saklanır.

Yeni hafta eklemek için: `data/` altına yeni dosyayı koyun ve `data/index.json` içindeki `issues` listesinin başına bir satır ekleyin.

## Okunma ve tıklanma sayacı (isteğe bağlı)

Site GoatCounter ile sayfa görüntülenmesini ve her haberin kaynak bağlantısına kaç kez tıklandığını sayabilir. Çerez kullanmaz, kişisel veri toplamaz.
1. goatcounter.com'da ücretsiz hesap açın, bir kod seçin (ör. `fraudbulten`).
2. Settings bölümünde "Allow adding visitor counts on your website" seçeneğini açın.
3. `index.html` içindeki `const GOATCOUNTER = "";` satırına kodu yazın.
Sayılar sayfada haberlerin altında görünür; ayrıntılı istatistikler GoatCounter panelindedir.

## GitHub Pages

Settings → Pages → Source: "Deploy from a branch" → Branch: `main`, klasör: `/ (root)` → Save.
Site birkaç dakika içinde `https://selinuluca.github.io/Fraud-Bulten/` adresinde yayına girer.
