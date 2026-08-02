# KMY MMD-1

Eğri çizici, osiloskop ve multimetre aynı kutuda. Kart üstünde arıza ararken
bileşeni sökmeden ölçüm alır; iki probu karşılaştırır, sağlam bir kartla arızalı
olanı yan yana koyar.

Bu depo cihazın bilgisayar uygulamasının ve yazılım güncellemelerinin dağıtıldığı
yerdir. Cihazın kaynak kodu burada değildir.

**İndirme ve kurulum:** https://kmyelectronicseu-png.github.io/kmy-mmd1/

## Kısaca

Kurulum dosyasını [Sürümler](../../releases/latest) sayfasından indirin,
çalıştırın. Yönetici şifresi sormaz. Cihazı USB ile takıp uygulamada Bağlan
deyin; cihaz açılışta kendi denetimini yapar, ilk on beş saniye komut kabul
etmez.

Kablosuz kullanmak isterseniz USB'yi çıkarın. Cihaz `KMY MMD-1` adında şifresiz
bir ağ yayınlar; o ağa bağlanınca ayar sayfası açılır (açılmazsa tarayıcıya
`192.168.4.1` yazın). Kendi ağınıza katma, sabit IP verme ve fabrika ayarlarına
dönme işlemleri orada.

## Güncelleme

Uygulama yeni sürümü kendisi görür ve Ayarlar → Cihaz altında haber verir.
Onaylarsanız indirir, kurar, yeniden açılır.

Cihazın yazılımı da aynı yerden güncellenir. `.ctfw` uzantılı dosya cihaz
yazılımı paketidir; içinde hem ana kartın hem Wi-Fi modülünün yazılımı vardır ve
hangisinin güncellenmesi gerekiyorsa uygulama onu yazar. Kalibrasyon kaydınız
silinmez. İşlem sırasında kabloyu çıkarmayın.

Bir sürüm size uymadıysa eskisine dönebilirsiniz, hepsi listede durur.

Paketler şifrelenmiş ve imzalıdır. Cihaz doğrulamadan tek bayt yazmaz; dosyayı
indiren biri içindeki yazılımı çıkaramaz.

## Destek

Seri numaranız uygulamada Ayarlar → Cihaz altında yazıyor. Bize yazarken
eklerseniz işimizi kolaylaştırırsınız.

---
KMY Electronics
