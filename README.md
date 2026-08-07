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

---

## Kurulum

Bilgisayarda kurulum dosyasını indirip doğrudan çalıştırın; yönetici parolası
istemez.

Telefonda APK dosyasını indirip üstüne dokunun. Android, mağaza dışından
uygulama kurmaya izin vermenizi ister — telefonun ayarlarından bu izni
vermezseniz kurulum başlamaz.

Cihazın ihtiyacı olan her şey, cihaz yazılımı dahil, bu uygulamaların içinde
gelir. Ayrıca indirilecek bir şey yoktur.

## Cihaza bağlanmak

Bilgisayar cihaza USB kablosuyla bağlanır. Telefon ise WiFi ile: cihazı ya
mevcut bir WiFi ağınıza alırsınız, ya da cihaz kendi WiFi ağını yayınlar ve
telefonu doğrudan o ağa bağlarsınız. Ağın olmadığı yerde ikincisi işinizi
görür; ayrı bir yönlendirici gerekmez.

> **Cihaz aynı anda tek bağlantıya hizmet eder.** USB ile WiFi'den yalnız
> birinden bağlanabilirsiniz — ikisi birden olmaz. USB kablosu takılıyken cihaz
> WiFi modülünü bilerek uyutur, çünkü ölçüm devresinin yanında yayın yapan bir
> radyo okumaları bozar.

**WiFi kurulumu** cihaza nasıl bağlıysanız oradan yapılır — USB'den de, ağ
üzerinden de. Uygulamada **Ayarlar → WiFi Kurulumu**'nu açıp ağ adı ile şifreyi
gönderirsiniz; uygulama cihazı ağda bularak kurulumun tuttuğunu doğrular. Aynı
yerden sonradan ağı değiştirebilir ya da güncelleyebilirsiniz.

Kutudan çıktığı hâliyle cihaz **KMY MMD-1** adlı şifresiz bir ağ yayınlar. Yani
bilgisayar olmadan da kurulabilir: telefonu o ağa bağlayın, uygulamayı açıp
**Bağlan** deyin, sonra WiFi kurulumundan cihazı kendi ağınıza alın. Sabit IP
gibi ileri ayarlar için cihazın kendi kurulum sayfası da var (tarayıcıda
`192.168.4.1`).

Kurulumdan sonra uygulama güncellemeleri kendisi denetler ve onayınızla kurar.
Eski sürümler [yayınlar sayfasında](https://github.com/kmyelectronicseu-png/kmy-mmd1/releases).

---

## Installation

On a PC, download the installer and run it. It never asks for an administrator
password.

On a phone, download the APK and tap it. Android will ask you to allow installs
from outside the store — the install will not start until you grant that
permission in the phone's settings.

Everything the device needs, firmware included, comes inside these
applications. There is nothing else to download.

## Connecting to the device

A PC connects over USB. A phone connects over Wi-Fi: either you put the device
on your existing network, or the device broadcasts its own and the phone joins
that. The second is what you want where there is no network — no separate
router needed.

> **The device serves one connection at a time.** You can connect over USB or
> over Wi-Fi, not both. While the USB cable is plugged in, the device
> deliberately puts its Wi-Fi module to sleep — a radio transmitting next to
> the measurement front end disturbs the readings.

**Wi-Fi setup** is done from whatever connection you already have — over USB or
over the network, either works. Open **Settings → Wi-Fi Setup** in the app and
send the network name and password; the app confirms the setup by finding the
device on the network. You can change or update the network from the same place
later.

Out of the box the device broadcasts an open network called **KMY MMD-1**, so
no PC is needed: join the phone to it, open the app, press **Connect**, then
move the device onto your own network from Wi-Fi Setup. For advanced settings
such as a static IP the device also serves its own setup page at
`192.168.4.1`.

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

## Ne yapar / What it does

- **Eğri testi** — bileşene bir sinyal uygular, eğriyi çizer, ne olduğunu
  söyler. Direnç, kondansatör, bobin, diyot, zener.
- **Kart kaydı ve testi** — kartın fotoğrafı üzerinde test noktaları
  işaretlenir, her noktanın eğrisi kaydedilir. Şüpheli kart bu kayda karşı
  denetlenir; uyumsuz noktalar fotoğrafta kırmızı görünür.
- **Osiloskop** — iki kanal, 5,5 kS/s, son yirmi saniye geriye sarılabilir.
- **Multimetre** — iki prob aynı anda, DC/AC kendiliğinden.

---

© KMY Electronics
