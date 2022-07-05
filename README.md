# Enhanced-Conversions-Kurulumu
Enchanced Conversion Kurulumu Hakkında Detaylı Bilgiler


//Enhanced Conversion kod yapısı
dataLayer.push({
    "event": "enhanced_conversion_data",
    "email": "deneme@roipublic.com", //dinamik olarak gelen kullanıcının e-posta adresi
    "phone_number": "+905551112233", //dinamik olarak gelen telefon numarası, +90 ile başlamalı ve boşluk içermemeli,
    "address": {
        "first_name": "Ahmet", //dinamik olarak gelen kullanıcının ismi
        "last_name": "Mehmet", //dinamik olarak gelen kullanıcının soyismi
        "street": "sokak adres", //dinamik olarak gelen kullanıcının sokak bilgisi
        "city": "İstanbul", //dinamik olarak gelen kullanıcının şehir bilgisi
        "region": "Şişli", //dinamik olarak gelen kullanıcının ilçe bilgisi
        "postal_code": "34045", //dinamik olarak gelen kullanıcının posta kodu
        "country": "TR", //dinamik olarak gelen kullanıcının ülke kodu
    }
});
