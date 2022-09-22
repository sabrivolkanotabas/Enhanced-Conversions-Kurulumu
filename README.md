#  Google Ads Enhanced Conversions Kurulumu


![Anatomi](https://github.com/anatomi-data/Analytics-Enhanced-Ecommerce/blob/main/anatomi-png.png)

#

Google'ın cookiesiz dönem için şimdiden uygulamaya koyduğu yeni bir beta var: Enhanced Conversions.

Enhanced Conversions aracılığıyla ilgili web sitesinde dönüşüm gerçekleştiren kullanıcının ad, adres, telefon numarası gibi verilerini alabiliyoruz.
Ardından bu verileri karma halinde kullanarak dönüşüm ölçümleme işlemini iyileştirebiliyoruz.

Örneğin dönüşüm kodlarında bir problem olduğunda, kullanıcılar çerezlere izin vermediğinde veya 3rd party araçlar ile takip etmemizi engellediklerinde eğer kullanıcı Google'a login olmuş ise bu kullanıcılar Enhanced Conversion ile takip edilebilecek.

Bu özellik 3 yoldan entegre edilebiliyor: Google Tag Manager, Manuel Ekleme ya da API aracılığıyla.
Biz burada Google Tag Manager üzerinden kurulumu yapacağız. Bunu yapabilmemiz için yazılım ajansının satın alma sayfanıza aşağıda ilettiğim kod parçasını event olarak göndermesi lazım.


```javascript
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
    'event': "enhanced_conversion_data",
    
    // Google Ads Enhanced Ecommerce Parametreleri
    // ❗ Aşağıdaki verilerin tamamı kullanıcıdan zorunlu alınıyorsa gönderilsin.
    // Eğer bir tanesi bile zorunlu değilse o zaman "address" objesi gönderilmesin, sadece email ve phone_number gönderilsin. 
    
    'enhanced_conversion_data': {
        "email": 'E-mail adresi',
        "phone_number": '+90 555 111 22 33',
        "address": {
            "first_name": 'İsim',
            "last_name": 'Soyisim',
            "street": 'Sokak',
            "city": 'İl',
            "region": 'İlçe',
            "postal_code": 'Posta Kodu',
            "country": 'Ülke'
        }
    }
});
```
