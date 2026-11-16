# Fraud & Teknoloji Bülteni

Dünyadan ve Türkiye'den haftanın en önemli 10 fraud, siber güvenlik ve AI/teknoloji haberi. Her haber en fazla üç cümlede Türkçe özetlenir. Her Pazartesi akşamı güncellenir.

## Yapı

- `index.html`: site. En son haftayı gösterir, geçmiş haftalar açılır listeden seçilir. Derleme adımı yoktur.
- `data/index.json`: hafta listesi, en yenisi en üstte.
- `data/YYYY-AA-GG.json`: o haftanın 10 haberi (yayın tarihiyle adlandırılır).
- `kaynaklar.md`: taranan kaynaklar ve seçim ölçütleri.
- `EDITORYAL.md`: haber seçimi ve özet yazımı için yayın ilkeleri.

## Haftalık dosya biçimi

```json
{
  "date": "2026-11-16",
  "label": "9–16 Kasım 2026",
  "items": [
    {
      "title": "Türkçe başlık",
      "summary": "En fazla 3 cümle.",
      "category": "fraud | siber | ai",
      "region": "tr | dunya",
      "source": "Kaynak adı",
      "url": "https://...",
      "more": [{ "source": "İkinci kaynak (isteğe bağlı)", "url": "https://..." }],
      "date": "2026-11-13"
    }
  ]
}
```

Yeni hafta eklemek için: `data/` altına yeni dosyayı koyun ve `data/index.json` içindeki `issues` listesinin başına bir satır ekleyin.

## GitHub Pages

Settings → Pages → Source: "Deploy from a branch" → Branch: `main`, klasör: `/ (root)` → Save.
Site birkaç dakika içinde `https://selinuluca.github.io/Fraud-Bulten/` adresinde yayına girer.
