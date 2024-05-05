# RoboDog-Byte

RoboDog-Byte, bir robot köpek prototipi için geliştirilmiş bir kod ve donanım projesidir. Bu projenin amacı, bir robotun denge sağlama yeteneklerini, hareket etme yeteneklerini ve belirli görevleri yerine getirme yeteneklerini araştırmak ve geliştirmektir.

## Kullanılan Mekaniklerin Açıklamaları

### `motor_set` Sınıfı
Bu sınıf, motor pin bilgilerini saklar ve her bir motor için kalibrasyon noktalarını yönetir.

**Dinamik():** 6 eksenli gyro-ivme sensöründen verileri alır ve robotun eğim değişimlerinde dengesini sağlayarak gövdesini düz tutmasını sağlar.
**swrite():** Motorlardan alınan PWM sinyallerini işler. Açı verilerini PWM sinyallerine dönüştürerek daha okunaklı bir kod yazılmasını sağlar.
**pos_cal():** Robotun tüm bacaklarını kalibrasyon için sıfır konumlarına getirir.
**kinematik():** Her bacağın gideceği konumu koordinat olarak alır. Gitmesi gereken konum için Femur, Tibia ve Coxa açılarını hesaplar. Ayak uçlarını istenilen konuma açı verisi alınmadan kendisi hesaplayarak götürür.



![286881295-137f41aa-8408-4518-a000-63a4fb4cac94](https://github.com/ibrahimTlmcu/RoboDog-Byte/assets/94108626/eaff163b-2f59-4954-b69f-d71328e849ae)

https://github.com/ibrahimTlmcu/RoboDog-Byte/assets/94108626/c2f13c07-0834-4f1c-bef6-d7cbad1dcf16



https://github.com/ibrahimTlmcu/RoboDog-Byte/assets/94108626/7f078bbf-c35a-4928-9961-0b57fc96cb2f



