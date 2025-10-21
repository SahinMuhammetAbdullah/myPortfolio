---
# BENZERSİZ PROJE KİMLİĞİ: 
# Bu ID, projenin farklı dillerdeki versiyonlarını birbirine bağlar.
# Her iki dildeki .md dosyasında da AYNI olmalıdır.
# Küçük harf, rakam ve tire (-) kullanın. Boşluk veya özel karakter kullanmaktan kaçının.
id: urldet 

# SIRALAMA:
# Projelerin ana sayfada hangi sırada görüneceğini belirler (isteğe bağlı).
# Küçük sayılar daha önce gelir.
order: 1

# BAŞLIK (Dil Spesifik):
# Projenin bu dildeki başlığı. Modal penceresinde ve proje kartında görünür.
title: "URLDet | Zararlı URL Analizi"

# KISA AÇIKLAMA (Dil Spesifik):
# Proje kartında görünecek kısa, bir veya iki cümlelik özet.
short_description: "Makine Öğrenimi ve Pekiştirmeli Öğrenme kullanılarak bir tarayıcı eklentisi ve web adresi üzerinden sorgulama ekranı uygulaması."

# ETİKETLER (Dil Spesifik olabilir veya ortak tutulabilir):
# Projede kullanılan ana teknolojiler veya anahtar kelimeler. 
# Proje kartında ve modalda gösterilebilir.
tags: ["Python", "Makine Öğrenimi", "Pekiştirmeli Öğrenme", "JavaScript", "React JS"]

# PROJE KARTI GÖRSEL AYARLARI (Kapak resmi yoksa kullanılır):
image_gradient_from: "ctp-blue"   # Renk geçişinin başlangıç rengi (Tailwind renk sınıfı)
image_gradient_to: "ctp-sapphire" # Renk geçişinin bitiş rengi

# PROJE KARTI İKONU:
# Kapak resmi yoksa veya kapak resminin üzerinde küçük bir ikon olarak gösterilir.
# Font Awesome sınıfını kullanın.
icon_class: "fa-solid fa-blog"

# KAPAK GÖRSELİ (İsteğe Bağlı):
# Proje kartında gösterilecek ana görsel. Eğer bu alan varsa, image_gradient_* alanları kullanılmaz.
# Yol, projenizin kök dizinine göre olmalı ve başında / olmalı.
cover_image: "/assets/images/projects/urldet-img.png" # 1920*960 pixel

# LİNKLER:
# github_url: "https://github.com/SahinMuhammetAbdullah/portfolio-site" # Projenin GitHub deposu (varsa)
live_url: "https://urldet.masahin.dev" # Projenin canlı demo adresi (varsa)

layout: default
description: "Makine Öğrenimi ve Pekiştirmeli Öğrenme kullanılarak bir tarayıcı eklentisi ve web adresi üzerinden sorgulama ekranı uygulaması."
image: /assets/images/projects/urldet-img.png
lang: tr
---

## Çalışma Prensibi

1 milyondan fazla URL verisi üzerinde gerçekleştirilen testler ve eğitimler sonucunda %97’nin üzerinde doğruluk oranına sahip bir sistem geliştirilmiştir. 

### Sistem iki aşamalı bir yapıya sahiptir:

1. Zararlılık Tespiti (Binary Classification):
İlk aşamada, girilen URL’nin zararlı (malicious) ya da zararsız (benign) olup olmadığı belirlenir. Bu aşamada Random Forest, SVM ve Naive Bayes gibi klasik makine öğrenimi algoritmaları karşılaştırılmış ve en yüksek doğruluk oranını veren model seçilmiştir.

2. Zararlı Türünün Belirlenmesi (Multi-class Classification):
Zararlı olarak tespit edilen URL’ler, ikinci aşamada Pekiştirmeli Öğrenme (Reinforcement Learning) yöntemiyle analiz edilerek phishing, malware veya defacement gibi kategorilere ayrılır. Bu süreçte model, ödül-ceza mekanizması sayesinde sürekli olarak kendini iyileştirir ve yeni tehdit tiplerine karşı adaptasyon sağlar.

Ek olarak, sistemde yer alan kara liste modülü, zararlı olduğu tespit edilen URL’lerin tekrar analiz edilmesini önleyerek işlem yükünü azaltır.

Proje kapsamında geliştirilen tarayıcı eklentisi, kullanıcıların ziyaret etmek istedikleri bağlantıların güvenliğini gerçek zamanlı olarak değerlendirir ve arama sonuçlarında URL’nin durumunu simgelerle gösterir. Ayrıca web tabanlı arayüz sayesinde kullanıcılar, herhangi bir URL’yi manuel olarak sorgulayabilir ve detaylı analiz raporuna erişebilirler.

Bu sayede URLDet, hem son kullanıcılar hem de güvenlik analistleri için güçlü, ölçeklenebilir ve kendini sürekli geliştiren bir siber güvenlik çözümü sunmaktadır.