# KMY MMD-1 — Kullanım Kılavuzu

**Çok Fonksiyonlu Ölçüm Cihazı**

Bir kutuda üç alet: bileşenleri gerilim–akım eğrisinin biçiminden tanıyan bir
eğri çizici, iki kanallı bir osiloskop ve iki kanallı bir voltmetre. Windows
bilgisayara USB ile bağlanır, ağ kurulumundan sonra kablosuz da çalışır.
Android telefon ve tabletlerde de aynı uygulama kullanılır.

> English version: [user-guide-en.md](user-guide-en.md)

---

## İçindekiler

1. [Gerekenler](#1-gerekenler)
2. [Yazılımın kurulumu](#2-yazılımın-kurulumu)
3. [İlk bağlantı](#3-ilk-bağlantı)
4. [Ana pencere](#4-ana-pencere)
5. [Eğri Testi](#5-eğri-testi)
6. [Karşılaştırma](#6-karşılaştırma)
7. [Kart Kaydı ve Kart Testi](#7-kart-kaydı-ve-kart-testi)
8. [Osiloskop](#8-osiloskop)
9. [Multimetre](#9-multimetre)
10. [Ayarlar](#10-ayarlar)
11. [Kalibrasyon](#11-kalibrasyon)
12. [Kablosuz kullanım](#12-kablosuz-kullanım)
13. [Telefonda kullanım](#13-telefonda-kullanım)
14. [Güncellemeler](#14-güncellemeler)
15. [Güvenlik ve sınırlar](#15-güvenlik-ve-sınırlar)
16. [Bir şeyler ters giderse](#16-bir-şeyler-ters-giderse)

---

## 1. Gerekenler

Cihaz, USB kablosu ve 64 bit Windows 10 ya da 11 çalıştıran bir bilgisayar.
Kablosuz kullanacaksanız Android 7.0 ve üzeri bir telefon veya tablet de
yeter. Başka bir şey gerekmez: cihaz gücünü USB portundan alır, yazılım
yönetici parolası sormadan kurulur.

**Prob değdirmeden önce**, test edeceğiniz devrenin enerjisi kesik ve
kondansatörleri boşalmış olmalı. Eğri çizici problara kendi test sinyalini
basar; enerjili bir devre o sinyale karşı koyar ve iki taraf da zarar görür.

---

## 2. Yazılımın kurulumu

### Windows

1. Yayın sayfasını açın:
   <https://github.com/kmyelectronicseu-png/kmy-mmd1/releases/latest>
2. **KMY-MMD-1-Kurulum.exe** dosyasını indirin.
3. Çalıştırın. İlk ekran kurulumun hangi dilde ilerleyeceğini sorar. Bu seçim
   yalnız kurulumu ilgilendirir; uygulamanın kendi dil ayarı ayrıdır ve
   istediğiniz zaman değiştirilir.
4. Sihirbazı geçin. Kurulum kendi kullanıcı klasörünüze yapılır, bu yüzden
   Windows yönetici parolası istemez.

Cihazın ihtiyacı olan her şey, cihaz yazılımı dahil, bu tek dosyanın içinde
gelir. Ayrıca indirilecek bir şey yoktur. Kurulum dosyasının yanındaki `.imza`
dosyası onun imzasıdır; uygulama sonradan indirdiği güncellemeleri bununla
doğrular, sizin bir şey yapmanız gerekmez.

### Android

Aynı yayın sayfasından **KMY-MMD-1-Mobil.apk** dosyasını telefona indirin ve
üstüne dokunun. Android mağaza dışından kuruluma izin vermenizi ister; çıkan
uyarıda "bu kaynağa izin ver" dedikten sonra kurulum devam eder. Uygulama
Android 7.0 ve üzeri, 64 bit ARM cihazlarda çalışır.

Mobil uygulama cihaza yalnız WiFi ile bağlanır — telefonda USB bağlantısı
yoktur. Bunun tek gerçek sonucu, cihaz yazılımının telefondan
güncellenememesi; ölçüm tarafında eksik bir şey yok. Ayrıntı için
[Telefonda kullanım](#13-telefonda-kullanım).

---

## 3. İlk bağlantı

USB kablosunu takın ve **KMY MMD-1** uygulamasını açın. Cihaz pencerenin
üstündeki listede belirir, **Bağlan** düğmesine basın.

Cihaz her açılışta ilk iş kendini dahili gerilim referanslarına göre ölçer.
Bu on beş saniye kadar sürer; o sırada denetimler kilitli kalır ve çıkış
açılmaz. Yapılacak bir şey yok, beklemek yeterli. Bağlantı durumunun yanındaki
nokta yeşile döndüğünde cihaz hazırdır.

Kabloyu takar takmaz bağlanmayı denediyseniz cihaz henüz açılışını bitirmemiş
olabilir. Birkaç saniye sonra tekrar deneyin.

---

## 4. Ana pencere

![Ana pencere](images/tr/01_curve_tracer.png)

| # | Nedir |
|---|---|
| 1 | Cihaz adı, bağlantı durumu ve Bağlan / Bağlantıyı Kes düğmesi. |
| 2 | Üç alet: Eğri Testi, Osiloskop, Multimetre. |
| 3 | Ayarlar — dil, cihaz bilgileri, WiFi, güncelleme, kalibrasyon. |
| 4 | Basit / Gelişmiş. Basit en çok işe yarayan üç ayarı gösterir, Gelişmiş geri kalanını açar. |
| 5 | Test ayarları: bileşene uygulanan tepe gerilim, frekans ve akım kademesi. |
| 6 | Hangi probun sürüldüğü: Prob 1, Prob 2 ya da ikisi birden. |
| 7 | Grafiğin ne çizdiği: V-I eğrisi, gerilim/zaman, akım/zaman ya da ikisi alt alta. |
| 8 | Grafik. Eksenler seçtiğiniz gerilim ve akım kademesine göre kurulur. |
| 9 | Çıkış anahtarı ve yanındaki kırmızı acil durdurma. |
| 10 | Karşılaştırma, Kart Kaydı ve Kart Testi — birine basınca açılır. |
| 11 | Sonuç: cihazın bileşeni ne sandığı ve değerleri. |

Eksenler ölçtüğünüz şeye göre büyüyüp küçülmez; seçtiğiniz ayarlardan
hesaplanır. Böylece bir eğrinin ekranda kapladığı yer bir şey ifade eder ve
iki ölçümü gözle karşılaştırabilirsiniz.

Sol panelin altındaki **Görünürlük** başlığında üç anahtar var: **Referans**
kayıtlı referans eğriyi grafiğin üstüne bindirir, **Eşdeğer Devre** sonucun
altına cihazın karar verdiği devreyi çizer, **Dondur** ekrandaki eğriyi olduğu
gibi tutar.

Kırmızı acil durdurma çıkışı keser ve bütün kademeleri anında bırakır. Cihaz
bağlıysa her zaman çalışır; kalibrasyon yokken bile. Bir şey ters göründüğünde
tereddüt etmeyin.

---

## 5. Eğri Testi

Aletin ana işi budur. Bileşene alternatif bir gerilim uygular ve akan akımı,
onu doğuran gerilime karşı çizer. Her bileşen ailesi farklı bir biçim çizer;
o biçim bileşenin kimliğidir.

### İşin özü olan üç ayar

**Gerilim** — test sinyalinin tepe değeri. Basit panelde dört basamak var:
2,5 V, 5 V, 10 V ve 15 V (Düşük, Orta-1, Orta-2, Yüksek). Gelişmiş panelde
0,1 V'tan 15 V'a kadar sürekli ayarlanır. Bilmediğiniz bir parçada düşükten
başlayın ve eğri düz kalıyorsa yükseltin. Diyot ve transistör eklemleri iletim
eşiğini geçecek kadar gerilim ister, kondansatör ve direnç istemez.

**Frekans** — 10, 50, 100 ve 1000 Hz hazır basamakları, gelişmişte 1–1000 Hz
arası serbest ayar. Kondansatör ve bobini dirençten ayıran şey budur.
Direncin eğrisi frekansla oynamaz. 100 nF'lık bir kondansatör 10 Hz'de ince,
neredeyse kapalı bir dilim çizer; 1 kHz'e çıktığınızda düzgün bir elipse
açılır. Elinizdekinin kondansatör olduğunu doğrulamanın en hızlı yolu
frekansı çevirip açıklığın değiştiğini görmektir.

**Akım kademesi** — aletin ne kadar akım görmeye hazırlandığı.

| Kademe | Ne için |
|---|---|
| Hassas | Kondansatörler, büyük dirençler, çok az akım çeken her şey. |
| Orta | Bilmediğiniz bir parçada iyi bir başlangıç. |
| Yüksek | Küçük dirençler, iletimdeki diyotlar, çok akım çeken her şey. |

Eğri tepesinden kesilmiş görünüyorsa ya da uygulama sinyalin sınırda olduğunu
söylüyorsa gerilimi düşürün veya bir kaba kademeye geçin. Tersi de sık olur:
az akım çeken bir parçayı Yüksek kademede ölçerseniz eğri yassı bir çizgiye
dönüşür ve parçayı açık devre sanırsınız. Şüphede kaldığınızda kademeyi
Hassas'a alıp bir daha bakın.

### Eğriyi okumak

- **Ortadan geçen eğik çizgi** — direnç. Ne kadar dikse direnç o kadar küçük.
- **Yatay eksende yatan çizgi** — açık devre, ya da problara bir şey değmiyor.
- **Dik çizgi** — kısa devre.
- **Elips** — kondansatör. Açıklık büyüdükçe değer büyür.
- **Diz (kıvrım)** — diyot ya da bir eklem. Dizin gerilim ekseni üzerindeki
  yeri iletim eşiğidir: silisyum bir diyotta 0,6 V dolayında, Schottky'de daha
  solda, LED'de belirgin biçimde sağda.
- **İki tarafta da diz** — zener, ya da ters bağlı iki eklem. Sağdaki iletim,
  soldaki delinme gerilimidir; zeneri seçerken 15 V'un altındakileri
  görebilirsiniz, üstündekiler için cihazın gerilimi yetmez.

Grafiğin altındaki sonuç kartı bulduğu şeyi adlandırır, değerini verir ve ne
kadar emin olduğunu söyler. **Eşdeğer Devre** açıkken karar verdiği devreyi de
çizer.

Kart üzerindeki bir bileşeni ölçtüğünüzde gördüğünüz eğri o bileşenin değil,
ona paralel duran her şeyin toplamıdır. Sonuç kartının "direnç" dediği yerde
aslında bir direnç, bir bobin ve yarım devre olabilir. Kesin karar vermeniz
gereken yerde bir bacağı kaldırın.

### Gelişmiş denetimler

![Gelişmiş panel](images/tr/02_advanced.png)

| # | Nedir |
|---|---|
| 1 | Basit / Gelişmiş geçişi. |
| 2 | Dalga formu: Sinüs, Üçgen, Kare, Testere, DC. Eğri testinin standardı sinüstür; DC sabit gerilim uygular. |
| 3 | Tepe gerilim, kaydırma çubuğu ve sayı olarak. 0,1–15 V; DC seçiliyken −15…+15 V. |
| 4 | Frekans; hazır basamaklar (10, 50, 100, 1k) ve 1–1000 Hz kaydırma çubuğu. |
| 5 | Manuel bias — sinyalin merkezini sıfırdan kaydırır. Kapalı gelir ve neredeyse her iş için kapalı doğrudur. |
| 6 | Uygula. Cihaza gönderilmeyi bekleyen değişiklik varsa belirir. |

Bunların altındaki **Akım Kademesi** bölümü gelişmiş panelde iki satırdır:
Prob 1 ve Prob 2 ayrı ayrı ayarlanır. İki probu karşılaştıracaksanız
kademeleri eşitleyin. Farklı kademedeki iki eğri hiçbir zaman uyuşmaz, üstelik
aynı parçalara bakıyor olsanız bile.

### Otomatik tespit ve Otomatik Optimize Et

**Otomatik** açıkken uygulama probları dinler. Bir bileşene değdiğinizde
türünü tanır ve o türü en iyi gösteren gerilim, frekans ve kademe üçlüsüne
geçer. Aynı sonucu üst üste üç kez görmeden karar vermez, bu yüzden temas
titrerken ayarlar ileri geri atlamaz. Karar verdikten sonra siz probu kaldırıp
başka bir parçaya değene kadar yeniden arama yapmaz.

Bilinmeyen parçalarla dolu bir tepsiyi elden geçirmenin en hızlı yolu budur.
Buna karşılık kart testinde kapalı tutun: her noktada ayarları değiştirmesi,
noktaların kaydedildiği ayarlarla karşılaştırılmasını bozar.

**Otomatik Optimize Et** aynı aramayı, o an probda duran parça için siz
basınca bir kez yapar. Arama işe yarar bir sonuç bulamazsa ayarlara dokunmaz
ve sonuç alanında **Tanımlanamadı** yazar.

### Tarama

**Tarama modu** üç eksenden birini — gerilim, frekans ya da akım kademesi —
basamak basamak gezer ve siz durdurana kadar döner. Diğer iki ayar yerinde
kalır. Her basamakta yarım saniye kadar bekler, kademe taramasında röle
otursun diye biraz daha uzun.

Elinizde ne olduğunu bilmediğiniz bir parça varsa frekans taramasıyla
başlayın: eğrisi frekansla değişiyorsa reaktif bir şey, değişmiyorsa dirençsel
bir şeydir. Taramayı durdurduğunuzda başlangıçtaki gerilim, frekans ve kademe
geri gelir.

### İki prob

**Prob 1** ve **Prob 2** tek seferde tek probu sürer. **Senkron** ikisini aynı
kaynaktan aynı anda sürer; iki bileşeni tek turda karşılaştırmanın yolu budur.

---

## 6. Karşılaştırma

![Karşılaştırma](images/tr/03_compare.png)

| # | Nedir |
|---|---|
| 1 | Karşılaştırma çekmecesini açar. |
| 2 | Kapalı, Canlı ↔ Referans ya da Prob 1 ↔ Prob 2. |
| 3 | Referansın hangi probdan yakalanacağı. |
| 4 | Referansı Yakala — ekrandaki eğriyi ölçüt olarak saklar. |
| 5 | Referansı dosyaya kaydet, kayıtlı bir referansı geri yükle ya da sil. |

**Canlı ↔ Referans** probun o an değdiği şeyi daha önce yakaladığınız bir
eğriyle karşılaştırır. **Prob 1 ↔ Prob 2** iki probu birbiriyle karşılaştırır:
birine sağlam olduğunu bildiğiniz parçayı, diğerine şüpheliyi bağlarsınız.
İkincisi daha güvenilirdir, çünkü iki ölçüm aynı anda, aynı sıcaklıkta ve aynı
ayarlarla yapılır. Bunun için iki probun da açık ve bir kademeye ayarlanmış
olması gerekir.

Karar, sizin belirlediğiniz eşiğe göre bir benzerlik yüzdesidir. Eşiğin üstü
**EŞLEŞTİ**, altı **EŞLEŞMEDİ** okur. Fabrika eşiği %90; sıradan bir işte iyi
bir yerdir. Yükselttikçe alet titizleşir, düşürdükçe hoşgörülü olur.

Kayıtlı bir referansı geri yüklediğinizde uygulama onun test ayarlarını da
uygular. Referans 5 V, 100 Hz ve Orta kademede alınmışsa karşılaştırma da öyle
yapılır; başka türlüsü anlamsız olurdu.

**Sesli uyarı**yı açın, gözünüzü ekranda değil kartta tutabilirsiniz. Sürekli
ötmez, yalnız karar değiştiğinde öter. Eşiğin tam sınırında gidip gelen bir
ölçümde sürekli çalmasın diye küçük bir tolerans bırakılmıştır.

Bir de şu var: hiçbir prob ölçülebilir akım çekmiyorsa uygulama "eşleşti"
demez, **ÖLÇÜM YOK** yazar. İki tane gürültü birbirine çok benzer ve bu
benzerlik hiçbir şey ifade etmez. Bu uyarıyı görüyorsanız ya prob temas
etmiyordur ya da kademe o parça için fazla kabadır.

**Kritik bölge hassasiyeti** üç kademelidir: Kapalı, Normal, Yüksek.
Karşılaştırmayı eğrinin kıvrım bölgelerinde sıkılaştırır, çünkü bileşenin
kimliği asıl orada saklıdır. Birbirine benzeyen iki parça arasındaki farkı
kovalarken Yüksek'e alın. Gündelik işte Normal'de bırakın; Yüksek'te sağlam
parçalar da kalmaya başlar.

---

## 7. Kart Kaydı ve Kart Testi

Tekrar göreceğiniz bir kartı test etmenin yolu budur: her test noktasını bir
kez kaydedin, sonra şüpheli kartı o kayda karşı denetleyin. Kaydı sağlam
olduğunu bildiğiniz bir karttan alın. Sağlam kart yoksa elinizdeki en iyisinden
alın, ama neyi kaydettiğinizi not düşün.

![Kart Kaydı](images/tr/08_board_record.png)

| # | Nedir |
|---|---|
| 1 | Kayıt ile test arasında geçiş. |
| 2 | Normal ölçüm ekranına dön. |
| 3 | Proje klasörünü seç. Bir karta ait her şey — fotoğrafı ve bütün test noktaları — tek klasörde durur. |

Proje klasörü taşınabilir: fotoğraf klasörün içine kopyalanır, noktalar
klasördeki dosyalarda tutulur. Klasörü olduğu gibi başka bir bilgisayara
kopyalayıp orada açabilirsiniz.

### Bir kartı kaydetmek

1. Bir proje klasörü seçin ve karta bir ad verin.
2. Kartın fotoğrafını ekleyin. Tepeden ve düz ışıkta çekilmiş bir fotoğraf
   işinizi kolaylaştırır; eğik çekilmiş fotoğrafta noktaları doğru yere
   koymak zordur.
3. Probu test noktasına değdirin, fotoğrafta o yere dokunun, noktaya ad verin
   ve **NOKTAYI KAYDET** deyin. O andaki eğri, noktanın referansı olur. Kayıt
   için çıkışın açık ve ölçümün akıyor olması gerekir.
4. Kartın üzerinde ilerleyin. İşaretçinin boyutu ve şekli nokta başına
   ayarlanır; sık bacaklı bölgelerde küçüğünü seçin, noktalar üst üste
   binmesin.

Noktaya ad verirken kartın kendi baskısını kullanın: R14, C7, U3-1. Altı ay
sonra "sol üstteki" hiçbir şey ifade etmiyor.

**Çok kademeli imza**, her noktayı tek ayar yerine üç dört gerilim ve frekans
kademesinde kaydeder: aynı noktanın yarım genlikte, dört kat frekansta ve
dörtte bir frekanstaki hâli de saklanır. Kayıt daha uzun sürer, ama böyle
kaydedilmiş bir noktayı kandırmak çok daha zordur. Tek ayarda birbirinin
aynısı görünen iki bileşen bütün ayarlarda nadiren aynı görünür.

Kartı kaydettikten sonra cihazı yeniden kalibre ederseniz kayıtlarınız geçerli
kalır; uygulama eski eğrileri yeni kalibrasyona göre yeniden yerleştirir.

### Bir kartı test etmek

![Kart Testi](images/tr/09_board_test.png)

**Kart Testi**'ni açın, **Testi başlat** deyin ve noktaları sırayla dolaşın.
Her nokta ölçülür, referansıyla karşılaştırılır ve geçti ya da kaldı olarak
işaretlenir. Uyumsuz noktalar kart fotoğrafında kırmızı görünür; elinize bir
liste değil, arızanın haritası geçer.

Duraklatabilir, ulaşamadığınız bir noktayı atlayabilir ya da testi erken
bitirebilirsiniz. Atlanan noktalar ayrı sayılır — ne geçti ne kaldı — ve özet
bunu açıkça yazar. Testi bitirdikten sonra **Kalanları test et** ile yalnız
geriye kalanlara dönebilirsiniz.

**Oto Mod**, nokta eşleşince kendiliğinden sıradakine geçer. Karar vermeden
önce üst üste beş temiz eşleşme arar; başlıktaki sayaç kaçta kaç olduğunu
gösterir. Probu tutup ekrana değil karta bakmak istediğinizde açın.

İş bitince **Excel Raporu Oluştur** bütün turu yazar. Rapor üç sayfadır:
nokta nokta ayrıntı (kartın kırpılmış fotoğrafı, ayarlar, eğri ve karar), bir
özet tablosu ve geçti/kaldı haritası.

---

## 8. Osiloskop

![Osiloskop](images/tr/04_scope.png)

| # | Nedir |
|---|---|
| 1 | Çalıştır/durdur, tek yakalama ve OTO. |
| 2 | Zaman tabanı ve kullanılan örnekleme hızı. |
| 3 | Dalga, FFT ya da XY görünümü. |
| 4 | Ekranı PNG, görünen veriyi CSV olarak kaydet. |
| 5 | Canlı / İncele ve kayıtta gezinme düğmeleri. |
| 6 | Ekran. |
| 7 | Kanal ayarları: dikey ölçek, konum, AC/DC giriş, prob çarpanı, ters çevirme. |
| 8 | Tetikleme: kaynak, kenar, mod, seviye ve tetiğin ekrandaki yeri. |
| 9 | Ölçüm imleçleri. |
| 10 | İzden çıkarılan canlı ölçümler. |

Osiloskop kipinde sinyal çıkışı kapalıdır, problar yalnız dinler. Giriş 50 V'a
kadar ölçer.

Cihaz her zaman 5,5 kS/s örnekler; donanım sınırı budur ve zaman tabanını
değiştirmek onu değiştirmez, yalnız ekranda görünen pencereyi değiştirir.
Buradan çıkan pratik sonucu bilin: bu bir alçak frekans osiloskobudur. Besleme
dalgalanması, motor sürücü, sensör çıkışı, ses bandının altı gibi işlerde rahat
çalışır. Bir kilohertzin üstünde dönem başına yalnız birkaç örnek düşer ve
dalganın biçimi güvenilmez olur.

Zaman tabanı 5 ms/kare ile 2 s/kare arasında, dikey ölçek 50 mV/kare ile
10 V/kare arasında ayarlanır.

**OTO**, ekrana sinyal getirmenin en hızlı yoludur: gelen sinyale bakıp zaman
tabanını, dikey ölçeği ve tetik seviyesini sizin yerinize kurar. Girişte
anlamlı bir sinyal yoksa gürültünün üstüne yakınlaşmaz, ayarları olduğu gibi
bırakır.

**Tetikleme** üç kipte çalışır. *Otomatik* tetik bulamasa da ekranı tazeler;
ne olduğunu bilmediğiniz bir sinyalde bununla başlayın. *Normal* yalnız tetik
geldiğinde çizer, ekran boş kalıyorsa seviyeniz yanlıştır. *Tek* bir kere
yakalar ve durur, bir defalık bir olayı beklerken kullanılır. Tetiğin ekrandaki
yatay yeri %10, %25 ya da %50 seçilebilir; %50 tetikten öncesini de görmenizi
sağlar.

**İncele** akışı durdurur ve son yirmi saniyede ileri geri gidip
yakınlaşmanıza izin verir. Kayıt siz canlı bakarken de sürdüğü için, "az önce
bir şey oldu" dediğinizde o şey hâlâ oradadır. Yirmi saniyeden eskisi düşer.

Bir kanalı kapatınca cihaz bütün ölçüm bütçesini diğerine verir ve iz gözle
görülür biçimde temizlenir. Örnekleme hızı yine 5,5 kS/s'tir; değişen, her
örneğin kaç ölçümün ortalaması olduğudur. Kullanmadığınız kanalı kapatın.

**FFT** yalnız etkin kanalı çizer; hangisi olduğunu İmleçler bölümündeki
"Etkin kanal" belirler. **XY** için iki kanalın da açık olması gerekir: Kanal 1
yatay, Kanal 2 dikeydir.

Alt çubukta dört ölçüm hazır gelir (Vpp, Ort, Vrms, Frekans). Listede on bir
tane var; Vmin, Vmax, AC Vrms, Periyot, Doluluk, Yükselme ve Düşme de
eklenebilir. Frekans okuması gürültüde kapanır: ölçtüğü dönemler birbirini
tutmuyorsa cihaz sayı uydurmak yerine boş bırakır.

**Prob çarpanı** yalnız gösterilen sayıyı ölçekler. ×10 bir prob taktıysanız
buradan ×10 seçin, yoksa bütün okumalarınız onda bir çıkar.

---

## 9. Multimetre

![Multimetre](images/tr/05_multimeter.png)

| # | Nedir |
|---|---|
| 1 | REL, MIN/MAX ve HOLD. |
| 2 | Prob 1 kartı: okuma, AC/DC göstergesi ve probun açma/kapama anahtarı. |
| 3 | Prob 2 kartı. |
| 4 | Okumanın ±50 V ölçeği içindeki yeri. |
| 5 | Okumaların hangi kalibrasyonu kullandığı. |

İki prob da aynı anda gerilim okur. Kademe düğmesi yok, fonksiyon düğmesi de
yok: cihaz sinyale bakıp DC mi AC mi olduğuna kendisi karar verir ve kartın
köşesinde hangisini gösterdiğini yazar. DC'de işaret de görünür.

- **REL** o anki okumayı sıfır kabul eder. Prob ve kablo düşümünü ölçümün
  dışında bırakmak ya da bir referansa göre fark okumak için.
- **MIN/MAX** gördüğü en küçük ve en büyük okumayı biriktirir; yanında beliren
  **SIFIRLA** sayacı temizler.
- **HOLD** ekranı dondurur.

REL ile MIN/MAX iki proba birden uygulanır, HOLD bütün ekranı dondurur.

Bu kipte de çıkış kapalıdır. Ölçtüğünüz probu açık bırakın: kapalı bir probun
ucu havada kalırsa okuduğu şey gerilim değil, kablonun topladığı gürültüdür.

Ölçüm penceresi sinyale göre kendini ayarlar. DC'de saniyenin onda biri kadar,
alçak frekanslı AC'de daha uzun; en az sekiz tam dönem bekler. 1 Hz'lik bir
sinyali bile doğru okur, yalnız okumanın oturmasını beklemeniz gerekir.

---

## 10. Ayarlar

![Ayarlar](images/tr/06_settings_device.png)

| # | Nedir |
|---|---|
| 1 | Dil — Türkçe ya da İngilizce. Anında değişir ve hatırlanır. |
| 2 | Cihaz ve Kalibrasyon sekmeleri. |
| 3 | Cihaz kimliği: yazılım sürümü, cihaz numarası, kalibrasyon durumu, WiFi modülünün durumu. |
| 4 | WiFi kurulumu. |
| 5 | Güncelle — uygulamayı ve cihaz yazılımını birlikte denetler. |
| 6 | Hakkında: hangi sürümleri kullandığınız. |

**WiFi modülü** satırına bir göz atmakta fayda var. Cihaz USB'deyken *uykuda*
yazmalı. Analog ön ucun yanı başında yayın yapan bir radyo gerilim
referanslarını bozar, bu yüzden cihaz USB'ye takılıyken modülü bilerek
uyutur. Ağ üzerinden bağlıysa elbette uyanıktır. Bunun bir yan etkisi var:
USB takılıyken cihazın kendi kurulum sayfasına erişemezsiniz.

**Cihaz no**yu destekle konuşurken isteriz; buradan kopyalayabilirsiniz.

Panelin altında **Servis / Tanılama** başlığı duruyor. Oradaki sayılar — alınan
kare sayısı, kayıp paket, öz denetim sonucu, referans okumaları — bir arıza
peşindeyken işe yarar, gündelik kullanımda bakmanız gereken bir şey değildir.

---

## 11. Kalibrasyon

![Kalibrasyon](images/tr/07_settings_cal.png)

| # | Nedir |
|---|---|
| 1 | Dil. |
| 2 | Kalibrasyon durumu, nereden okunduğu ve kaç nokta taşıdığı. |
| 3 | Kalibrasyonu Başlat. |

Kalibrasyon bilgisayarda değil **cihazın belleğinde** durur ve her bağlantıda
oradan okunur. Yani aletle birlikte gezer: başka bir bilgisayara taktığınızda
da, telefondan bağlandığınızda da kalibre kalır.

**Gerekenler:** probu kısa devre edecek bir kablo ve doğruluğuna güvendiğiniz
bir multimetre. O multimetrenin doğruluğu bu aletin doğruluğu olur; elinizdeki
en iyisini kullanın.

Sihirbaz beş aşamada ilerler ve birkaç dakika sürer:

1. **Açık devre** — iki prob da boşta, hiçbir şeye değmiyor. Akım kanallarının
   sıfırları ve osiloskop taban çizgisi ölçülür, yarım dakika kadar sürer.
2. **Prob 1 kısa** — Prob 1'in ucunu GND ile birleştirin. Yirmi saniye.
3. **Prob 2 kısa** — aynısı Prob 2 için.
4. **Okuma kalibrasyonu** — cihaz sırayla dört DC seviye sürer. Her seviyede
   Prob 1'in ucunu kendi multimetrenizle ölçüp okuduğunuz değeri yazarsınız.
   Aletin okumasını güvendiğiniz bir referansa bağlayan adım budur ve
   sihirbazın en önemli aşamasıdır.
5. **Çıkış kalibrasyonu** — cihaz çıkışını −15 V'tan +15 V'a birer volt adımla
   tarar ve artık kalibre olan okumasıyla kendini düzeltir. Kırk beş saniye
   kadar; problar bu sırada boşta olmalı.

Sonda isteğe bağlı bir aşama daha sorulur: osiloskop okumasının kalibrasyonu.
Bu, doğruluğuna güvendiğiniz **harici** bir gerilim kaynağı ister, çünkü
osiloskop kipinde cihaz kendi çıkışını süremez. Böyle bir kaynağınız yoksa
atlayın; osiloskop okuması düzeltmesiz kalır, geri kalan her şey çalışır. İki
ayrı gerilimde nokta alırsanız hem kazanç hem kayma çözülür, tek noktayla
yalnız kazanç düzelir.

Her onay ekranı bir önceki aşamayı tekrarlamanıza izin verir; yanlış bir ölçüm
baştan başlamayı gerektirmez. Sihirbazı yarıda iptal eder ya da kapatırsanız
cihaz elindeki eski kalibrasyonla çalışmayı sürdürür. Cihaza hiçbir şey tur
bitmeden yazılmaz.

Ne zaman yeniden kalibre edilir? Okumalar güvendiğiniz bir multimetreden gözle
görülür biçimde ayrılmaya başladığında, ya da uygulama referans tabanının
kalibrasyon anındakinden kaydığını bildirdiğinde. Onun dışında bir daha
dokunmanız gerekmez.

---

## 12. Kablosuz kullanım

Cihaz ağa iki türlü girer: ya sizin mevcut WiFi ağınıza katılır, ya kendi ağını
yayınlar. Hangisi işinize gelir, çalışma yerinize bağlı. Atölyede bir ağ varsa
ona katılsın; bilgisayarınız hem internete hem cihaza aynı anda bağlı kalır.
Ağ yoksa ya da sahadaysanız cihaz kendi ağını yayınlasın, bilgisayar veya
telefon doğrudan ona bağlansın. Ayrı bir yönlendirici gerekmez.

**Uygulamadan kurmak için** cihaza bağlanın, **Ayarlar → WiFi Kurulumu**'nu
açın, bağlantı yöntemini seçin, ağ adı ile şifreyi girin ve gönderin. Cihaz ağa
katılır; uygulama onu orada bularak kurulumu doğrular. Bu sırada cihaz bir süre
**MEŞGUL** görünebilir, normaldir.

**Cihazın kendi sayfasından kurmak için** önce USB kablosunu çıkarın — kablo
takılıyken WiFi modülü uyuduğu için sayfaya erişilmez. Kutudan çıktığı hâliyle
cihaz **KMY MMD-1** adlı şifresiz bir ağ yayınlar. Telefonunuzu ya da
dizüstünüzü bu ağa bağlayın; kurulum sayfası kendiliğinden açılır, açılmazsa
tarayıcıya `192.168.4.1` yazın. Sabit IP gibi ileri ayarlar yalnız orada
bulunur.

Cihaz ağa girdikten sonra uygulamada **WiFi**'ye geçip **Bağlan** deyin; aynı
ağdaki cihazlar kendiliğinden listelenir. Liste boş kalsa bile Bağlan çalışır:
bilgisayar cihazın kendi ağındaysa doğrudan 192.168.4.1 denenir.

Birkaç şey bilmekte fayda var:

- Bir cihaz aynı anda tek bağlantıya hizmet eder. Kullanımdaki bir cihaz
  listede **MEŞGUL** görünür; telefonla bilgisayarı aynı cihaza aynı anda
  bağlayamazsınız.
- Ağ ayarını ağ üzerinden değiştirirseniz cihaz yeni ağa geçerken bu bağlantı
  kopar. Beklenen davranış budur, cihazı yeni ağında yeniden bulmanız gerekir.
- Tek WiFi adaptörü olan bir dizüstü, cihazın kendi ağına bağlandığı anda
  internetten kopar. Telefonda bu daha az sorun olur, mobil veri açık kalır.
- Ayarları unutturmak isterseniz **Ağ ayarlarını sıfırla** cihazı fabrika
  durumuna döndürür: yine "KMY MMD-1" ağını yayınlamaya başlar.

---

## 13. Telefonda kullanım

Windows'ta kullandığınız uygulamanın aynısı Android'de de çalışır. Ölçüm
tarafında eksik yoktur: eğri testi, osiloskop, multimetre, karşılaştırma, kart
kaydı ve kart testi hepsi vardır. Ekran dar olduğu için düzen değişir. Üstteki
düğme Eğri Testi ile Osiloskop arasında geçiş yapar; karşılaştırma, kart
işleri, ayarlar ve kalibrasyon araç çubuğundaki anahtar simgesinin altında
toplanır.

Telefon cihaza yalnız WiFi ile bağlanır. Cihaz henüz hiçbir ağa girmemişse
telefonu cihazın kendi **KMY MMD-1** ağına bağlayın, uygulamayı açıp **Bağlan**
deyin. Bağlandıktan sonra **Ayarlar → WiFi Kurulumu** ile cihazı atölye ağınıza
alabilirsiniz; ayar cihaza yazıldığı anda bu bağlantı kopar, cihazı yeni
ağında yeniden bulursunuz.

**Cihaz yazılımı telefondan güncellenemez.** Yazma işi USB ister ve telefonda
USB yoktur. Cihaz yazılımı için bir Windows bilgisayara ihtiyacınız olur.

Uygulamanın kendi güncellemesi telefonda da çalışır, biraz farklı olarak:
**Güncelle** APK'nın adresini tarayıcıda açar, indirmeyi ve kurmayı Android
kendi yapar. Uygulamanın APK'yı doğrudan kurabilmesi için istemesi gereken izin
bir ölçüm aleti için fazla geniştir; istemiyoruz.

İki küçük ayrıntı: ölçüm sürerken telefonun ekranı kendiliğinden kararmaz, ve
dışa aktardığınız dosyalar (PNG, CSV, Excel raporu) telefonda uygulamanın kendi
klasörüne yazılır. Windows'ta bu klasör **Belgeler\KMY MMD-1**'dir.

---

## 14. Güncellemeler

**Ayarlar → Güncelle** hem uygulamayı hem cihaz yazılımını denetler ve eskiyen
ne varsa kurar. Kalibrasyonunuza dokunulmaz.

- Uygulama güncellemesi cihaz takılı olsa da olmasa da çalışır.
- Cihaz yazılımı USB bağlantı ister; ağ üzerinden ya da telefondan yazılamaz.
- İnternet yoksa denetim bunu söyler, hiçbir şey bozulmaz.

Cihaz yazılımı ayrıca indirilmez, uygulamanın kurulumuyla birlikte gelir.
Uygulamayı güncellediğinizde cihaz yazılımı da elinize geçmiş olur.

Yeni bir sürüm çıktığında bir kez sorulur. "Bu sürümü bir daha sorma"
diyebilirsiniz; daha yenisi çıktığında yine sorulur.

**Cihaz yazılımı yazılırken USB kablosunu çıkarmayın.** Yazma bitince cihazın
bağlantısı kesilir ve yeniden bağlanmanız gerekir, bu normaldir.

---

## 15. Güvenlik ve sınırlar

| | |
|---|---|
| Test gerilimi | ±15 V tepe |
| Test frekansı | 1–1000 Hz |
| Osiloskop / voltmetre girişi | 50 V'a kadar |
| Osiloskop örnekleme | 5,5 kS/s |
| Osiloskop derin kaydı | son 20 saniye |
| Besleme | USB portundan |

- **Kartı enerjisi kesikken** ve kondansatörleri boşalmışken test edin.
- Alet yalnız Eğri Testi kipinde sinyal sürer. Osiloskop ve Multimetre
  kiplerinde çıkış kapalıdır, problar yalnız dinler.
- Kırmızı acil durdurma çıkışı keser ve bütün kademeleri anında bırakır.
- Cihaz açılışını bitirene ve içinde kayıtlı bir kalibrasyon olana kadar çıkış
  anahtarı açılmaz.
- Buradaki hiçbir şey şebeke gerilimi için tasarlanmadı. Probları şebekeye
  değdirmeyin.

---

## 16. Bir şeyler ters giderse

**Cihaz listede görünmüyor.**
Kabloyu kontrol edin, başka bir USB portu deneyin. Windows'un adaptör için bir
USB-seri sürücüsüne ihtiyacı var; çoğu sistemde zaten kuruludur. Telefonda
liste yalnız ağdaki cihazları gösterir, USB oradan görünmez; bu bir arıza
değil.

**Bağlandıktan hemen sonra denetimler kilitli.**
Cihaz açılış öz-kalibrasyonunu yapıyor. On beş saniye kadar sürer ve
kendiliğinden açılır.

**Çıkış anahtarı açılmıyor.**
Cihaz ya hâlâ açılıyordur ya da içinde kayıtlı kalibrasyon yoktur. Ayarlar →
Kalibrasyon'u açıp duruma bakın.

**Eğri düz.**
Problara bir şey değmiyor, bileşen açık devre, ya da gerilim eşiğe ulaşacak
kadar yüksek değil. Gerilimi bir basamak artırın veya daha hassas bir akım
kademesine geçin. Kart üzerinde ölçüyorsanız prob ucunun lehim maskesine değil
gerçekten metale değdiğinden emin olun.

**Karşılaştırma sürekli ÖLÇÜM YOK diyor.**
Hiçbir prob ölçülebilir akım çekmiyor. Prob temasını kontrol edin; yüksek
empedanslı bir parça için Hassas kademeye geçin.

**Cihaz MEŞGUL görünüyor.**
Başka bir bağlantı onu kullanıyor — bir telefon ya da başka bir bilgisayar.
Önce onu kapatın.

**Okumalar kaymış görünüyor.**
Cihazı kapatıp açın; açılış öz-kalibrasyonu çoğu kaymayı toplar. Uygulama
referans tabanının kalibrasyon anındakinden ayrıldığını bildiriyorsa
kalibrasyonu yeniden yapın.

**Osiloskopta dalganın biçimi bozuk.**
Sinyalin frekansına bakın. 5,5 kS/s ile bir kilohertzin üstündeki bir dalganın
biçimini göremezsiniz, elinizde dönem başına birkaç nokta kalır.

**Telefon cihazı bulamıyor.**
Telefon ile cihaz aynı ağda mı? Cihaz kendi ağını yayınlıyorsa telefonu o ağa
bağlamanız gerekir, "bu ağda internet yok" uyarısını geçin.

---

## Destek

KMY Electronics — <https://github.com/kmyelectronicseu-png/kmy-mmd1>

Bize ulaşırken cihazın numarası işi kolaylaştırır: **Ayarlar → Cihaz →
Cihaz no**.
