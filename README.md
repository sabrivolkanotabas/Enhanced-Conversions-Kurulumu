#  Google Ads Enhanced Conversions Kurulumu


![Anatomi](https://github.com/anatomi-data/Analytics-Enhanced-Ecommerce/blob/main/anatomi-png.png)

#
 
Bu belgenin amacı, Google Ads Enhanced Conversion Kurulumu için gerekli dataLayer kodlarını entegre etmeye yardımcı olmaktır.

Ads EC kullanıcı bilgilerinden phone ve 

```javascript
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
    'event': "enhanced_conversion_data",
    'email': "denem@roipublic.com", 
    'phone_number': "+905551112233",
});
```
