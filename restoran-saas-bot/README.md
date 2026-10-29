# NodeDine WhatsApp Botu (ilk sürüm)

**NodeDine'ı restoran ve kafelere tanıtan, kod yazmadan n8n ile kurduğum ilk WhatsApp pazarlama botu.**

> Kaynak kodu gizli. Bu repo projenin ne yaptığını ve nasıl kurulduğunu anlatır.

---

## Ne yapıyordu

- Potansiyel restoran ve kafelere WhatsApp'tan otomatik tanıtım mesajı
- Gelen cevapları Gemini ile okuyup benim üslubumla cevap verme (ayrı bir persona dokümanıyla)
- Müşteri ikna olunca bana Telegram'dan bildirim
- Müşteri listesi ve durumları Google Sheets'te

## Kurgu

Dört ayrı n8n iş akışı:

| İş akışı | Görevi |
|---|---|
| Gelen mesaj işleyici | WhatsApp'tan gelen mesajı alır, yapay zekâya sorar, cevaplar |
| Giden mesaj gönderici | Listedeki işletmelere sırayla ilk mesajı atar |
| Telegram komutları | Botu Telegram'dan yönetme |
| Devretme bildiricisi | İkna olan müşteriyi bana bildirir |

## Teknoloji

n8n (kendi sunucumda) · Evolution API · Gemini 2.0 Flash · Google Sheets · Telegram Bot

## Sonrası

n8n ile hızlı başladım ama sınırlarına geldim. Botu sonradan kodla, panelli ve çok daha yetenekli şekilde yeniden yazdım: [Müşteri Bulucu Bot](../musteribulucu-bot).

---

[bycan.dev](https://bycan.dev) · [@bycandev](https://instagram.com/bycandev) · [Tüm projelerim](https://github.com/bycandev)
