---
id: project-lock 

order: 4

title: "Project Lock | Proje Yönetim Sistemi"

# KISA AÇIKLAMA (Video içeriği ile düzeltildi)
short_description: "C# Forms ve MySQL kullanılarak geliştirilmiş, kullanıcı bazlı erişim kontrolü sunan, proje, görev, çalışan yönetimi ve durum takibi (tamamlandı/gecikti) özelliklerine sahip bir masaüstü proje yönetim uygulaması."

# ETİKETLER (Video içeriği ile düzeltildi)
tags: ["C# Forms", "Windows Uygulaması", "MySQL", "Veritabanı Yönetimi", "Proje Yönetimi", "Görev Takibi"]

image_gradient_from: "ctp-blue"
image_gradient_to: "ctp-sapphire"

icon_class: "fas fa-lock" # Projenin adına uygun bir ikon seçildi

cover_image: "/assets/images/projects/project-lock.png"

github_url: "https://github.com/SahinMuhammetAbdullah/ProjectLock"
youtube_url: "https://www.youtube.com/watch?v=GyWu9BpimVg"

layout: default
description: "C# Forms ve MySQL kullanılarak geliştirilmiş, kullanıcı bazlı erişim kontrolü sunan, proje, görev, çalışan yönetimi ve durum takibi (tamamlandı/gecikti) özelliklerine sahip bir masaüstü proje yönetim uygulaması."
image: /assets/images/projects/project-lock.png
lang: tr
---

## Çalışma Prensibi

Project Lock, C# Forms platformunda geliştirilmiş bir masaüstü uygulamasıdır ve veri yönetimi için harici bir MySQL veritabanı kullanır. Projenin ana amacı, farklı kullanıcıların (yöneticiler) kendi projelerini, çalışanlarını ve görevlerini diğer kullanıcılardan izole bir şekilde yönetmesini sağlamaktır.

### 1. Temel Teknoloji ve Mimari

* **Ön Yüz (Frontend):** **C# Forms** kullanılarak geliştirilmiş, kullanıcıların tüm işlemleri yapabildiği görsel masaüstü arayüzünü sağlar.
* **Arka Yüz (Backend) ve Veritabanı:** Tüm veriler **MySQL** veritabanında depolanır ve yönetilir (MySQL portu açılıp PHPMyAdmin üzerinden kontrol edilmektedir).
* **Bağlantı ve İşlem:** C# kodu, bir `connection string` yapısı oluşturarak MySQL'e bağlanır ve tüm veri işlemlerini (kayıt, güncelleme, silme) **SQL sorguları** ile gerçekleştirir.

### 2. Veri Yapısı ve İlişkiler

Sistem, bir proje yönetiminin temelini oluşturan 4 ana tablo içerir:

* **User (Kullanıcı):** `User ID`, `username` ve `password` gibi temel giriş bilgilerini tutar.
* **Employee (Çalışan):** `Employee ID`, ad, soyad, bitirdiği ve devam eden proje sayısı gibi bilgileri içerir ve `User ID` ile bağlantılıdır (Foreign Key).
* **Project (Proje):** `Project ID`, isim, başlangıç ve bitiş tarihi gibi bilgileri içerir ve sahibini belirlemek için `User ID`'ye bağlıdır.
* **Task (Görev):** `Task ID`, görev ismi, başlangıç tarihi, **adam gün (adam gün değeri)**, bitiş tarihi ve durumu (status) gibi detayları tutar. Bu tablo, hangi çalışana atandığını belirtmek için `Employee ID` ve hangi kullanıcıya ait olduğunu belirtmek için `User ID`'ye bağlıdır.

### 3. Çalışma Prensibi (Kullanıcı İzolasyonu)

Projenin kritik çalışma prensibi, **Kullanıcı Bazlı İzolasyon**dur:

* Sistemde farklı kullanıcılar (yöneticiler) farklı kayıtlarla giriş yapabilir.
* Tüm tablolar (`Employee`, `Project`, `Task`) anahtar olarak **User ID**'ye bağlanır.
* Bu bağlantı sayesinde, farklı kullanıcılar sisteme girdiklerinde **birbirlerinin projelerine, çalışanlarına ve görevlerine ulaşamazlar**.

### 4. Yönetim Süreci

* **Proje Yönetimi:** Kullanıcılar, projelerine isim, başlangıç ve bitiş tarihi ekleyebilir, projeleri listeleyebilir.
* **Çalışan Yönetimi:** Çalışan kaydı oluşturulabilir, mevcut çalışanların isimleri/soyadları güncellenebilir ve kayıtları silinebilir.
* **Görev Yönetimi ve Takibi:** Projelere görevler eklenir. Bu görevlere adam gün değeri ve başlangıç/bitiş tarihleri atanır.
* **Durum Kontrolü:** Görevlerin son tarihleri kontrol edilir ve görevin durumu (`tamamlandı` gibi) güncellenir. Bu güncellemeler, çalışanın bitirdiği proje sayısını da etkiler.