---
id: sanayi-go 

order: 3

title: "SanayiGo | Bir Tarik-Tedarikçi Platformu"

short_description: "Flutter ve Firebase altyapısı kullanılarak geliştirilmiş, tedarikçilerin ürünlerini mobil ortamda sergileyebildiği ve alıcıların ürünler hakkında talep gönderebildiği hızlı bir B2B mobil ticaret platformu."

tags: ["Flutter", "Dart", "Firebase", "Firestore", "Mobil Uygulama", "Tedarik Zinciri"]

image_gradient_from: "ctp-blue"   
image_gradient_to: "ctp-sapphire" 

icon_class: "fa-solid fa-truck-field"

cover_image: "/assets/images/projects/sanayi-go.png" 

github_url: "https://github.com/SahinMuhammetAbdullah/sanayi_go" 
youtube_url: "https://www.youtube.com/watch?v=2XDAszjixOU"

layout: default
description: "Flutter ve Firebase altyapısı kullanılarak geliştirilmiş, tedarikçilerin ürünlerini mobil ortamda sergileyebildiği ve alıcıların ürünler hakkında talep gönderebildiği hızlı bir B2B mobil ticaret platformu."
image: /assets/images/projects/sanayi-go.png
lang: tr
---
## Çalışma Prensibi

SanayiGo, tedarikçiler ile alıcıları mobil ortamda bir araya getiren, modern ve bulut tabanlı bir mimari üzerine inşa edilmiştir. Uygulamanın çalışma prensibi, kullanıcı deneyimini önceliklendiren **Flutter** tabanlı ön yüz ile **Firebase**'in sunduğu hızlı ve ölçeklenebilir arka yüz servislerinin entegrasyonuna dayanır.

### 1. Ön Yüz (Frontend) - Flutter (Dart)

* **Platform:** Uygulamanın mobil arayüzü **Flutter (Dart)** kullanılarak geliştirilmiştir. Bu, tek bir kod tabanıyla hem Android hem de iOS cihazlarda çalışabilme imkanı sunar.
* **Mimari:** Proje, daha düzenli ve sürdürülebilir bir geliştirme için **Clean Code** ilkelerine uygun olarak tasarlanmıştır. Sayfalar, servisler, entity'ler (varlıklar) ve bileşenler birbirinden ayrılmıştır.
* **Temel Fonksiyon:** Kullanıcılara kayıt, giriş, ürünleri kategorilere göre listeleme, arama ve talep gönderme gibi tüm görsel etkileşimleri sunar.

### 2. Arka Yüz ve Veritabanı (Backend & Database) - Firebase

Uygulamanın tüm arka yüz hizmetleri, sunucusuz (serverless) bir çözüm olan **Google Firebase** tarafından sağlanır:

* **Kullanıcı Yönetimi (Firebase Authentication):** Kullanıcıların sisteme kayıt olması ve güvenli bir şekilde giriş yapması bu hizmet üzerinden yönetilir.
* **Veritabanı (Firestore):** Ürün detayları (isim, fiyat, kategori, ID) ve kullanıcı bilgileri **Firestore** NoSQL veritabanında depolanır. Ürün ekleme, silme ve detay görüntüleme gibi tüm işlemler doğrudan bu veritabanı üzerinden gerçekleştirilir.
* **Depolama (Firebase Storage):** Tedarikçilerin sisteme yüklediği ürün görselleri ve medya dosyaları bu alanda saklanır. Her fotoğrafın benzersiz bir ID'si bulunur.

### 3. Ana İş Akışı

Platform, iki ana kullanıcı rolü arasındaki iletişimi kolaylaştırır:

1.  **Tedarikçi (Ürün Ekleme):**
    * Tedarikçi, **Ürün Ekle** sayfasından ürün adı, kategorisi ve fiyatı gibi detayları girer 
    * Görseli eklenir ve veriler **Firestore**'a, görsel ise **Firebase Storage**'a yüklenir
    * Yüklenen ürünler, kullanıcının profil sayfasında listelenir ve buradan silinebilir

2.  **Alıcı (Talep Gönderme):**
    * Alıcı ana ekranda ürünleri kategorilere göre inceler veya arama çubuğunu kullanarak ilgili ürünü bulur.
    * İstenilen ürünü bulduğunda **"Talebe Gönderi"** butonuna basarak ürüne olan ilgisini belirtir.
    * Bu etkileşim sonucunda, ürünü ekleyen tedarikçinin hesabına anında bir bildirim gönderilir.

Bu bulut tabanlı yapı, uygulamanın düşük gecikme süresi ile çalışmasını ve artan kullanıcı sayısına kolayca ölçeklenebilmesini sağlar.