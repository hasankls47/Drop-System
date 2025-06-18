* 30 ⭐ paylaşılcaktır.

# CodeWorld Discord Drop System

CodeWorld Discord Drop System, Discord sunucunuzda otomatik olarak ödüllü "drop" etkinlikleri düzenlemenizi sağlayan bir bottur. Kullanıcılarınızla etkileşimi artırmak ve topluluğunuza heyecan katmak için tasarlanmıştır. Belirli aralıklarla, ayarladığınız kanalda rastgele ödüller dağıtabilir ve ilk tıklayan üyenin ödülü kazanmasını sağlayabilirsiniz.

## ✨ Özellikler

* **Otomatik Drop Gönderimi:** Belirlediğiniz zaman aralıklarında otomatik olarak drop başlatır.
* **Özelleştirilebilir Kanallar:** Dropların yapılacağı ve logların tutulacağı kanalları siz belirlersiniz.
* **Rol Etiketleme:** Drop duyurularında belirli bir rolü etiketleyebilirsiniz.
* **Ayarlanabilir Süreler:** Drop'un ne kadar süreyle aktif kalacağını (butona basma süresi) ve dropların hangi sıklıkta gönderileceğini ayarlayabilirsiniz.
* **Detaylı Loglama:** Kazananlar, ödüller ve drop zamanları gibi bilgileri log kanalında saklar.
* **Kolay Kurulum ve Yönetim:** Basit komutlarla tüm ayarları yönetebilirsiniz.
* **Etkileşimli Duyurular:** Yeni droplar, kazananlar ve kimsenin almadığı droplar için bilgilendirici mesajlar gönderir.

## 🖼️ Görsel Önizleme
<img src="https://fv5-3.files.fm/thumb_show.php?i=98jakpjedt&view&v=1&PHPSESSID=1700a090588820e3ba7a2b570595f252b7085dbe" width="45%"></img> 
<img src="https://fv5-3.files.fm/thumb_show.php?i=rv2kchm3v7&view&v=1&PHPSESSID=1700a090588820e3ba7a2b570595f252b7085dbe" width="45%"></img> 
<img src="https://fv5-3.files.fm/thumb_show.php?i=x76uxp3gpb&view&v=1&PHPSESSID=1700a090588820e3ba7a2b570595f252b7085dbe" width="45%"></img> 
<img src="https://fv5-3.files.fm/thumb_show.php?i=g6dnjzmjfe&view&v=1&PHPSESSID=1700a090588820e3ba7a2b570595f252b7085dbe" width="45%"></img> 
<img src="https://fv5-3.files.fm/thumb_show.php?i=4gz6d4ynhz&view&v=1&PHPSESSID=1700a090588820e3ba7a2b570595f252b7085dbe" width="45%"></img> 
<img src="https://fv5-3.files.fm/thumb_show.php?i=bn8tb9j4sc&view&v=1&PHPSESSID=1700a090588820e3ba7a2b570595f252b7085dbe" width="45%"></img> 

**Örnek Görüntüler:**

* **Drop Sistemi Ayarları ve Durum Değişiklikleri:**
    * `drop1.png` (Sistem durumu aktif/deaktif edildiğinde ve ayarlar güncellendiğinde gösterilen mesajlar)
    * `drop6.png` (Drop sistemi aktif edilemediğinde eksik ayarları gösteren uyarı)
* **Drop Akışı:**
    * `drop3.png` (Yeni bir drop geldiğinde kullanıcılara gösterilen mesaj ve "Drop Aç" butonu)
    * `drop4.png` (Bir kullanıcı drop'u kazandığında gösterilen mesaj)
    * `drop5.png` (Kimse drop'u almadığında gösterilen mesaj)
* **Loglama:**
    * `drop2.png` (Bir drop kazanıldığında log kanalına düşen kayıt)

## 🚀 Kurulum Adımları


1.  **İlk Ayarları Yapılandırın:** `/drop-ayar` komutunu kullanarak aşağıdaki temel ayarları yapın. Bot, eksik ayarlar olduğunda sizi uyaracaktır (`drop6.png` görselindeki gibi).
    * **Drop Kanalı:** Dropların gönderileceği metin kanalı.
    * **Drop Log Kanalı:** Drop etkinlikleriyle ilgili logların kaydedileceği metin kanalı.
    * **Etiketlenecek Drop Rolü:** Drop duyurularında etiketlenecek rol.
    * **Destek Kanalı:** (İsteğe bağlı) Kullanıcıların ödüllerini talep edeceği kanal (`drop4.png`'de `#destek` kanalı örneği verilmiş).
    * **Drop Gönderilme Sıklığı:** Dropların ne kadar sürede bir gönderileceği (örneğin, her 2 saatte bir).
    * **Drop Buton Süresi:** Kullanıcıların drop'a tıklamak için sahip olacağı süre (örneğin, 10 saniye).

    Örnek ilk ayar komutu (`drop1.png` ve `drop6.png`'den alınan bilgilere göre):
    ```
    /drop-ayar kanal:#drop-system log:#drop-log rol:@CodeWorld Drop System destek:#ticket-kanal gönderilmesüre:DAKİKA_SAYISI butonsüresi:SANİYE_SAYISI
    ```
    * `gönderilmesüre`: Değeri dakika cinsinden girin (örn: `120` = 2 saat).
    * `butonsüresi`: Değeri saniye cinsinden girin (örn: `10` = 10 saniye).

2.  **Sistemi Aktifleştirin:** Tüm ayarlar tamamlandıktan sonra `/drop-status` komutunu kullanarak sistemi aktif hale getirin. (`drop1.png`'de sistemin AKTİF edildiği görülüyor.)

## ⚙️ Bot Komutları

Aşağıda CodeWorld Drop System botunun temel komutları listelenmiştir:

### `/drop-ayar`
Drop sisteminin temel ayarlarını yapılandırmanızı sağlar. Daha önce ayarlanmışsa günceller.

**Parametreler:**
* `kanal:<#kanal_adı>`: (Zorunlu) Dropların gönderileceği metin kanalını belirtir. (Örn: `#drop-system`)
* `log:<#kanal_adı>`: (Zorunlu) Drop loglarının gönderileceği metin kanalını belirtir. (Örn: `#drop-log`)
* `rol:<@rol_adı>`: (Zorunlu) Drop duyurusunda etiketlenecek rolü belirtir. (Örn: `@CodeWorld Drop System`)
* `destek:<#kanal_adı>`: (Zorunlu, `drop6.png`'ye göre) Kullanıcıların ödül talebi veya destek için yönlendirileceği kanal. (Örn: `#ticket-kanal`)
* `gönderilmesüre:<dakika_cinsinden_süre>`: (Zorunlu) İki drop arasında geçecek süreyi dakika olarak ayarlar. (Örn: `60` yazarsanız 1 saatte bir drop atılır.)
* `butonsüresi:<saniye_cinsinden_süre>`: (Zorunlu) Drop butonunun aktif kalma süresini saniye olarak ayarlar. (Örn: `10` yazarsanız buton 10 saniye aktif kalır.)

**Örnek Kullanım (`drop1.png`'deki gibi):**

## <img src="https://cdn.discordapp.com/emojis/1036083490292244493.png" width="15px" height="15px">》Destek Sunucusu
[![DiscordBanner](https://invidget.switchblade.xyz/X62tP3fGax)](https://discord.gg/X62tP3fGax)

