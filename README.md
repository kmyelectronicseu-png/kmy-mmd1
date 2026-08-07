# KMY MMD-1

Bileşenleri gerilim–akım eğrisinden tanıyan bir eğri çizici, iki kanallı bir
osiloskop ve iki kanallı bir voltmetre. Tek kutuda, kendi yazılımıyla.

*A curve tracer that identifies components from their voltage–current curve, a
two-channel oscilloscope and a two-channel voltmeter — one instrument, with its
own software.*

---

## İndirin / Download

|  | Türkçe | English |
|---|---|---|
| **Bilgisayar**<br>Windows 10 / 11, 64 bit | [Kurulum dosyasını indir][win] | [Download the installer][win] |
| **Telefon ve tablet**<br>Android 7.0 ve üzeri | [APK dosyasını indir][apk] | [Download the APK][apk] |

[win]: https://github.com/kmyelectronicseu-png/kmy-mmd1/releases/latest/download/KMY-MMD-1-Kurulum.exe
[apk]: https://github.com/kmyelectronicseu-png/kmy-mmd1/releases/latest/download/KMY-MMD-1-Mobil.apk

**Türkçe.** Bilgisayarda kurulum dosyasını çalıştırıp sihirbazı geçin; yönetici
parolası istemez. Telefonda indirdiğiniz APK'ya dokunun, Android mağaza dışından
kuruluma izin vermenizi ister. Cihazın ihtiyacı olan her şey — cihaz yazılımı
dahil — bu dosyaların içinde gelir, ayrıca indirilecek bir şey yoktur.

Telefon cihaza yalnız WiFi ile bağlanır. Ölçüm tarafında eksik yoktur; tek
farkı, cihaz yazılımının telefondan güncellenememesidir.

Uygulama kurulduktan sonra güncellemeleri kendisi denetler ve onayınızla kurar.
Eski sürümler [yayınlar sayfasında](https://github.com/kmyelectronicseu-png/kmy-mmd1/releases).

**English.** On a PC, run the installer and work through the wizard; it never
asks for an administrator password. On a phone, tap the APK you downloaded —
Android will ask you to allow installs from outside the store. Everything the
device needs, firmware included, comes inside these files. There is nothing
else to download.

The phone reaches the device over Wi-Fi only. Nothing is missing on the
measurement side; the one difference is that device firmware cannot be updated
from a phone.

Once installed, the app checks for updates itself and installs them with your
say-so. Older versions are on the
[releases page](https://github.com/kmyelectronicseu-png/kmy-mmd1/releases).

---

## Kullanım kılavuzu / User guide

| | |
|---|---|
| **Türkçe** | [docs/user-guide-tr.md](docs/user-guide-tr.md) |
| **English** | [docs/user-guide-en.md](docs/user-guide-en.md) |

Ekran görüntüleriyle, baştan sona. Uygulamanın içinden de açılır:
**Ayarlar → Belgeler**.

*Screenshots throughout, start to finish. Also reachable from inside the app:
**Settings → Documentation**.*

---

## Kutudan çıkanlar / What it does

- **Eğri testi** — bileşene bir sinyal uygular, eğriyi çizer, ne olduğunu
  söyler. Direnç, kondansatör, bobin, diyot, zener.
- **Kart kaydı ve testi** — kartın fotoğrafı üzerinde test noktaları
  işaretlenir, her noktanın eğrisi kaydedilir. Şüpheli kart bu kayda karşı
  denetlenir; uyumsuz noktalar fotoğrafta kırmızı görünür.
- **Osiloskop** — iki kanal, 5,5 kS/s, son yirmi saniye geriye sarılabilir.
- **Multimetre** — iki prob aynı anda, DC/AC kendiliğinden.

---

© KMY Electronics
