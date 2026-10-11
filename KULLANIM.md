# 📖 Lordumelkor Game's Archive - Kullanım Rehberi

Bu arşivdeki oyunlar **Ready-to-Go (Doğrudan Oyna)** formatında derlenmiştir.

---

## 🚀 Oyunları Başlatma

1. İlgili oyunun kartındaki **"İndir"** butonuna tıklayın.
2. İndirilen `.zip` veya `.7z` arşivini [7-Zip](https://www.7-zip.org/) veya [WinRAR](https://www.rarlab.com/) ile bir klasöre çıkarın.
3. Klasörün içindeki ana `.exe` dosyasını çalıştırın.

---

## 🎮 Kontrolcü ve Gamepad Ayarları

- **Xbox & DualSense / PS4:** Çoğu oyun XInput veya SDL2 üzerinden kontrolcünüzü taktığınız anda otomatik olarak tanır.
- **Klavye & Fare:** FPS ve nişan alma oyunlarında (King Kong, Perfect Dark, GoldenEye) fare serbest bakış (mouselook) varsayılan olarak açıktır.
- Oyun içi grafik, çözünürlük veya tuş atamalarını genellikle açılış launcher ekranından ya da oyun içi `F1` / `Esc` menüsünden değiştirebilirsiniz.

---

## ➕ Yeni Oyun Ekleme (Override Sistemi)

Yeni çıkan bir recomp oyununu sisteme eklemek için `games.js` dosyasını değiştirmeden sadece `eklenen.js` dosyasını düzenleyebilirsiniz:

```javascript
window.EKLENEN_OYUNLAR.push({
  "id": "yeni-oyun-id",
  "title": "Oyunun Adı",
  "platform": "Nintendo 64",
  "genre": "Action",
  "size": "50 MB",
  "downloadUrl": "https://archive.org/download/...",
  "archiveUrl": "https://archive.org/details/...",
  "cover": "https://..."
});
```

---

## 🚫 Link Kaldırma / Gizleme

Bozulan veya kaldırılan bir oyunu arayüzden gizlemek için `kaldirilan.js` dosyasına oyunun `id` değerini yazmanız yeterlidir:

```javascript
window.KALDIRILAN_OYUNLAR.push("bozuk-oyun-id");
```
