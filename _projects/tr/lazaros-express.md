---
id: lazaros-express 

order: 2

title: "Lazaros Express | Bir E-Ticaret Platformu"

short_description: "Güvenli ödeme ve hızlı sipariş yönetimi özelliklerine sahip, Java tabanlı çok katmanlı (multi-tier) mimari kullanılarak geliştirilmiş kapsamlı bir e-ticaret platformu uygulaması."

tags: ["Java", "E-Ticaret", "Multi-Tier Mimari", "Veritabanı Yönetimi", "Web Uygulaması"]

image_gradient_from: "ctp-blue"
image_gradient_to: "ctp-sapphire"

icon_class: "fas fa-shopping-cart"

cover_image: "/assets/images/projects/lazaros-express.png"

github_url: "https://github.com/SahinMuhammetAbdullah/lazaros"
youtube_url: "https://www.youtube.com/watch?v=c_bx73bYhsI"

layout: default
description: "Güvenli ödeme ve hızlı sipariş yönetimi özelliklerine sahip, Java tabanlı çok katmanlı (multi-tier) mimari kullanılarak geliştirilmiş kapsamlı bir e-ticaret platformu uygulaması."
image: /assets/images/projects/lazaros-express.png
lang: tr
---

## Çalışma Prensibi

Lazaros Express E-Ticaret Platformu, güncel web uygulaması geliştirme standartlarına uygun olarak **Çok Katmanlı (Multi-Tier) Mimari** üzerine inşa edilmiştir. Bu yaklaşım, sistemin ölçeklenebilirliğini, güvenliğini ve sürdürülebilirliğini artırır. Proje, temel olarak aşağıdaki üç ana katmanın birbiriyle etkileşimi üzerine kuruludur:

### 1. Sunum Katmanı (Presentation Layer)

Bu katman, kullanıcıların doğrudan etkileşimde bulunduğu arayüzü sağlar.

* **Rolü:** Kullanıcı etkileşimlerini (ürün arama, sepete ekleme, giriş yapma) yönetir ve Uygulama Katmanından gelen verileri görselleştirir.
* **Teknolojiler:** HTML, CSS, JavaScript (ve muhtemelen React JS gibi bir kütüphane/framework) kullanılarak geliştirilmiştir. Depodaki `express` klasörü, bu katmanın web sunucusu veya API'ler ile olan bağlantı noktası olabilir.

### 2. Uygulama/İş Mantığı Katmanı (Application/Business Logic Layer)

Sistemdeki tüm e-ticaret kurallarının ve süreçlerinin yürütüldüğü merkezi kattır.

* **Rolü:** Sunum katmanından gelen istekleri işler, gerekli iş kurallarını (stok kontrolü, indirim hesaplama, sipariş doğrulama) uygular ve Veri Katmanından gerekli bilgileri ister/kaydeder.
* **Teknolojiler:** Büyük oranda **Java** dili kullanılarak geliştirilmiştir. Depodaki `Servers` klasörü, bu katmanın sunucu tarafındaki kodlarını ve iş mantığını barındırır. Bu katman, mikroservis veya modüler bir yapıya sahip olabilir.

### 3. Veri Katmanı (Data Layer)

Uygulamanın tüm kalıcı verilerinin saklandığı, erişildiği ve yönetildiği katmandır.

* **Rolü:** Ürün kataloğu, kullanıcı profilleri, sipariş geçmişleri, stok seviyeleri gibi kritik verileri güvenli bir şekilde depolamaktan ve Uygulama Katmanından gelen sorgulara yanıt vermekten sorumludur.
* **Teknolojiler:** `db` klasörünün varlığı, projenin bir veritabanı yönetim sistemi (PostgreSQL, MySQL veya MongoDB gibi) kullandığını gösterir. Uygulama, JDBC gibi araçlarla bu veritabanına erişim sağlar.

### İş Akışı Özeti

1.  **Talep:** Kullanıcı bir eylem gerçekleştirir (örneğin "Satın Al"). Bu talep Sunum Katmanı aracılığıyla HTTP isteği olarak gönderilir.
2.  **İşleme:** Uygulama Katmanı bu isteği yakalar, kullanıcı oturumunu doğrular ve ödeme/stok gibi iş mantığını çalıştırır.
3.  **Veri İletişimi:** İş Mantığı Katmanı, sipariş kaydını oluşturmak ve stok miktarını güncellemek için Veri Katmanı ile iletişim kurar.
4.  **Yanıt:** Veritabanından gelen onay ile İş Mantığı Katmanı işlemi tamamlar ve sonucu Sunum Katmanına gönderir.
5.  **Geri Bildirim:** Sunum Katmanı, kullanıcıya "Siparişiniz tamamlandı" gibi bir mesajı görüntüler.

Bu katmanlı yapı sayesinde, örneğin kullanıcı arayüzünü (Sunum Katmanı) değiştirmek, arka plandaki iş mantığını (Uygulama Katmanı) etkilemeden kolayca yapılabilir. Bu, e-ticaret platformunun bakımını ve gelecekteki ölçeklenmesini kolaylaştırır.