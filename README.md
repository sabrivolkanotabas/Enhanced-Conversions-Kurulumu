#  Google Ads Enhanced Conversions Kurulumu


![Anatomi](https://github.com/anatomi-data/Analytics-Enhanced-Ecommerce/blob/main/anatomi-png.png)

#
 
Bu belgenin amacı, Google Ads Enhanced Conversion Kurulumu için gerekli dataLayer kodlarını entegre etmeye yardımcı olmaktır.


Google'un cookiesiz dönem için şimdiden uygulamaya koyduğu yeni bir beta var: Enhanced Conversions.

Enhanced Conversions aracılığıyla web sitede dönüşüm gerçekleştiren kullanıcının ad, adres, telefon numarası gibi verilerini alabiliyoruz. Ardından bu verileri karma halinde kullanarak dönüşüm ölçümleme işlemini iyileştirebiliriz.

Dönüşüm kodlarında bir problem olduğunda, kullanıcılar çerezlere izin vermediğinde veya 3rd party araçlar ile takip etmemizi engellediklerinde eğer kullanıcı Google'a login olmuş ise bu kullanıcılar Enhanced Conversion ile tracking edilebilecek.

Üç yoldan entegre edilebiliyor bu özellik; GTM, Manuel ya da API aracılığıyla.

Biz burada GTM üzerinden kurulumu yapacağız. Bunu yapabilmemiz için satın alma sayfanıza aşağıda ilettiğim kod parçasını event olarak göndermesi lazım yazılım ajansının.


```javascript
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
    'event': "enhanced_conversion_data",
    
    // Google Ads Enhanced Ecommerce Parametreleri
    'enhanced_conversion_data': {
        "email": 'E-mail adresi',
        "phone_number": '+90 555 111 22 33',

        // ❗❗❗ Aşağıdaki veriler zorunlu alınıyorsa kullanıcılardan gönderilsin.
        // Eğer bir tanesi bile zorunlu değilse o zaman "address" objesi gönderilmesin, sadece email ve phone_number gönderilsin yeterlidir. 
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
