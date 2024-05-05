# RoboDog-Byte

RoboDog-Byte, bir robot köpek prototipi için geliştirilmiş bir kod ve donanım projesidir. Bu projenin amacı, bir robotun denge sağlama yeteneklerini, hareket etme yeteneklerini ve belirli görevleri yerine getirme yeteneklerini araştırmak ve geliştirmektir.

## Kullanılan Mekaniklerin Açıklamaları

### `motor_set` Sınıfı
Bu sınıf, motor pin bilgilerini saklar ve her bir motor için kalibrasyon noktalarını yönetir.

- **Dinamik():** 6 eksenli gyro-ivme sensöründen verileri alır ve robotun eğim değişimlerinde dengesini sağlayarak gövdesini düz tutmasını sağlar.
- **swrite():** Motorlardan alınan PWM sinyallerini işler. Açı verilerini PWM sinyallerine dönüştürerek daha okunaklı bir kod yazılmasını sağlar.
- **pos_cal():** Robotun tüm bacaklarını kalibrasyon için sıfır konumlarına getirir.
- **kinematik():** Her bacağın gideceği konumu koordinat olarak alır. Gitmesi gereken konum için Femur, Tibia ve Coxa açılarını hesaplar. Ayak uçlarını istenilen konuma açı verisi alınmadan kendisi hesaplayarak götürür.

## Kurulum
Projeyi yerel bir ortama klonlayın ve gerekli bağımlılıkları yükleyin.

```bash
git clone https://github.com/kullanici_adi/RoboDog-Byte.git
cd RoboDog-Byte
pip install -r requirements.txt
