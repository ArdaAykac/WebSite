# settings.json – KULLANIM TALİMATI (SON SÜRÜM)
# Olympic Juice Web Sitesi – JSON ile Tamamen Yönetilir
# Menü, logo, lokasyon, iletişim, addon → Sadece bu dosyayı düzenle!
# TARAYICIYI DOĞRUDAN AÇMA → SUNUCU BAŞLAT!

## 1. GENEL YAPI (TEMEL ŞABLON)
{
  "logo": "images/logo.png",
  "brand_name": "Olympic Juice",
  "hero_image": "images/hero-cup.png",
  "menu_title": "İmza Karışım Bardakları",
  "locations": ["Beşiktaş", "Kadıköy", "Şişli"],
  "contact": {
    "title": "Bize Ulaşın",
    "phone": "+90 555 123 45 67",
    "email": "info@olympicjuice.com",
    "address": "Beşiktaş, İstanbul",
    "social": [
      { "name": "Instagram", "url": "https://instagram.com/olympicjuice", "icon": "images/icons/instagram.png" },
      { "name": "X", "url": "https://x.com/olympicjuice", "icon": "images/icons/twitter.png" }
    ]
  },
  "items": [
    // BURAYA ÜRÜNLER GELİR
  ],
  "addons": [
    // BURAYA EKSTRA EKLEMELER GELİR
  ]
}

## 2. YENİ ÜRÜN EKLEME (items DİZİSİNE)

### ŞABLON:
{
  "item_name": "Ürün Adı",
  "item_image": "images/dosya_adi.png",
  "ingredients": "Malzeme1, Malzeme2",
  "fiyat": 99.99,
  "para_birimi": "TL"
}

### ÖRNEK:
"items": [
  {
    "item_name": "Portakal Suyu",
    "item_image": "images/portakalsuyu.png",
    "ingredients": "Taze sıkılmış portakal",
    "fiyat": 85.00,
    "para_birimi": "TL"
  },
  {
    "item_name": "Limonata",
    "item_image": "images/limonata.png",
    "ingredients": "Limon, nane, bal",
    "fiyat": 90.00,
    "para_birimi": "TL"
  }
]

### KURALLAR:
- Her ürün { } içinde
- Her üründen SONRA virgül (,) → SON ÜRÜNDEN SONRA VİRGÜL YOK!
- ingredients → İsteğe bağlı (boş bırakılabilir)
- fiyat → Ondalık nokta ile: 34.50
- item_image → images/ klasöründeki yol

## 3. ADDONS (EKSTRA EKLEMELER)

### ŞABLON:
{ "name": "Protein", "icon": "images/addons/protein.png" }

### ÖRNEK:
"addons": [
  { "name": "Protein", "icon": "images/addons/protein.png" },
  { "name": "Kollajen", "icon": "images/addons/kollajen.png" },
  { "name": "Limon", "icon": "images/addons/limon.png" }
]

### KURALLAR:
- İkonlar: images/addons/ klasörüne koy
- Her addondan sonra virgül → SON ADDONDAN SONRA VİRGÜL YOK!

## 4. İLETİŞİM BİLGİLERİ (YENİ!)

"contact": {
  "title": "Bize Ulaşın",
  "phone": "+90 555 123 45 67",
  "email": "info@olympicjuice.com",
  "address": "Beşiktaş, İstanbul",
  "social": [
    { "name": "Instagram", "url": "https://instagram.com/...", "icon": "images/icons/instagram.png" },
    { "name": "X", "url": "https://x.com/...", "icon": "images/icons/twitter.png" }
  ]
}

## 5. KLASÖR YAPISI (ZORUNLU!)

website/
├── index.html
├── settings.json
└── images/
    ├── logo.png
    ├── hero-cup.png
    ├── portakalsuyu.png
    ├── limonata.png
    └── addons/
        ├── protein.png
        ├── kollajen.png
        └── limon.png
    └── icons/                 YENİ
        ├── instagram.png
        └── twitter.png

## 6. SUNUCU BAŞLATMA (ZORUNLU!)

### TARAYICIYI DOĞRUDAN AÇMA → ÇALIŞMAZ!
### CORS HATASI ALIRSIN → JSON YÜKLENMEZ

### DOĞRU YOL:
1. Terminal aç 
2. Şu komutları sırayla yaz:

#Windows
cd  buraya  bu klasörü terminale sürükleyin önce cd yazın sonra  cd nin yanına klasörü sürükleyin entere basın
sonra  sunucuyu çalıştırın  terminalde python -m http.server 8000
python -m http.server 8000
#Linux
cd /home/arda/Masaüstü/website
python3 -m http.server 8000



googlede veya herhangi bir tarayıcda (html tabanlı tarayıcılarda geçerli) http://localhost:8000/website.html yazarak siteye ulaşabilirsiniz 
eğer  websiteadınız.com olarak erişmek istiyorsanız domaine ihtiyacınız var

TOKEN
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

######## Update Version-1.2
####AdminPanel
Bir sürü şeyler yapılıyor
https://ardaaykac.github.io/WebSite/#adminpanel 
yazarak panele ulaşabiliyorsunuz ve push butonuna basarsanız 2 dk içerisinde en son yaptığınız 
değişiklikler ile site update oluyor

TOKEN=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
Repo Sahibi = ArdaAykac
Repo Adı = WebSite
Branch = Version-1.2
bu bilgileri girdikten sonra istediğinizi yapabilirsiniz