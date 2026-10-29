# Yedekleme Servisi

**Veritabanlarını ve klasörleri otomatik olarak şifreleyip Google Drive'a yedekleyen, web panelli bağımsız servis.**

> Kaynak kodu gizli. Bu repo projenin ne yaptığını ve nasıl kurulduğunu anlatır.

---

## Neden yaptım

Projelerim kendi sunucumda çalışıyor. Sunucuda bir sorun olursa veri de gitmesin diye, yedeklediği sistemlerden tamamen bağımsız çalışan bir araç istedim.

## Ne yapıyor

Panelden kaynak eklersin (Postgres veritabanı ya da klasör), ne sıklıkla yedekleneceğini seçersin (dakika / saat / gün). Her yedekte:

1. Döküm alır (`pg_dump` / `tar`)
2. gpg ile AES-256 şifreler
3. Google Drive'a yükler (rclone)
4. Kayıt tutar (SQLite)
5. E-posta raporu atar: neyden ne yedeklendi, boyutu, başarılı mı, nereye gitti

## Güvenlik kararları

- Veritabanı ve SMTP şifreleri, yedek parolası diskte düz metin durmaz. Yönetici şifresinden türetilen bir ana anahtarla şifrelenir (envelope encryption)
- Ortam değişkeni olarak sadece yönetici kullanıcı adı ve şifresi gerekir, gerisi panelden
- Yeniden başlatmaya dayanıklı zamanlayıcı

## Teknoloji

Node.js 24 (yerleşik `node:sqlite`) · Express · EJS · pg_dump · gpg · rclone · Nodemailer · Docker

---

[bycan.dev](https://bycan.dev) · [@bycandev](https://instagram.com/bycandev) · [Tüm projelerim](https://github.com/bycandev)
