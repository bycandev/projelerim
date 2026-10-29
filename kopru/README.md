# Köprü

**Mac ile Windows arasında dosya, metin ve resmi anında aktaran, internet olmadan da çalışan kişisel araç.**

> Kaynak kodu gizli. Bu repo projenin ne yaptığını ve nasıl kurulduğunu anlatır.

---

## Sorun

Bir Mac'im ve bir Windows'um var. Aralarında sürekli bir şey taşımam gerekiyordu; WhatsApp, flaş bellek, e-posta hiçbiri pratik değildi.

## Ne yapıyor

- İki bilgisayarda da arka planda sessizce çalışır
- Aynı ağdayken (internet olsun olmasın) anında gönderim
- Hiç ağ yoksa telefon hotspot'u ile kurulan geçici ağda da çalışır
- Tek, kendi kendine yeten bir program; kurulum veya ek bağımlılık istemez

## Teknik kararlar

- İlk plan Tauri (Rust) idi. Windows'ta 4 GB derleyici kurulumu gerektirdiği için **Go**'ya geçtim: boşta ~15-25 MB RAM, tek dosya
- macOS sürümü GitHub Actions'ta derleniyor; Mac'e hiçbir geliştirici aracı kurmadan hazır uygulama olarak iniyor

## Teknoloji

Go · GitHub Actions (çok platformlu derleme)

---

[bycan.dev](https://bycan.dev) · [@bycandev](https://instagram.com/bycandev) · [Tüm projelerim](https://github.com/bycandev)
