# Arduino-Sicaklik-Kontrol-ve-Uyari-Sistemi
Bu proje, ortam sıcaklığını sürekli olarak izleyen ve belirlenen bir eşik değerin üzerine çıkıldığında otomatik olarak mekanik bir sistemi (Servo Motor) devreye sokan, aynı zamanda sesli ve ışıklı uyarı veren bir otomasyon sistemidir.

🚀 Özellikler

* **Gerçek Zamanlı İzleme:** DHT11 sensörü ile anlık sıcaklık takibi.
* **Akıllı Eşik Kontrolü:** Sıcaklık **27.7°C** (ayarlanabilir) seviyesini geçtiğinde sistem otomatik olarak "Aktif" moda geçer.
* **Mekanik Kontrol:** Eşik değeri aşıldığında Servo motor 0°'den 90°'ye yumuşak bir geçiş yapar (Otomatik pencere/fan kapağı simülasyonu).
* **Geri Bildirim Sistemi:**
    * **Görsel:** 16x2 I2C LCD ekran üzerinden anlık sıcaklık ve sistem durumu ("ACIK"/"KAPALI") takibi.
    * **Işıklı:** Güvenli sıcaklıkta **YEŞİL**, yüksek sıcaklıkta **KIRMIZI** LED yanar.
    * **İşitsel:** Durum değişimlerinde (Açılma/Kapanma) farklı tonlarda Buzzer uyarısı verir.
* **Stabil Başlangıç:** Servo motorun enerji verildiğinde titremesini önleyen özel başlangıç algoritması içerir.

🔌 Pin Bağlantı Şeması

Yazılımdaki tanımlamalara göre bağlantı listesi şöyledir:

* **DHT11 Sinyal:** Pin 8
* **Servo Motor:** Pin 9
* **Buzzer:** Pin 10
* **Yeşil LED:** Pin 12
* **Kırmızı LED:** Pin 13
* **LCD Ekran:** SDA -> A4, SCL -> A5 (Uno için)
