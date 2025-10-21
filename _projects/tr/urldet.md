---
id: urldet 

order: 1

title: "URLDet | Zararlı URL Analizi"

short_description: "Makine Öğrenimi ve Pekiştirmeli Öğrenme kullanılarak bir tarayıcı eklentisi ve web adresi üzerinden sorgulama ekranı uygulaması."

tags: ["Python", "Makine Öğrenimi", "Pekiştirmeli Öğrenme", "JavaScript", "React JS"]

image_gradient_from: "ctp-blue"
image_gradient_to: "ctp-sapphire"

icon_class: "fa-solid fa-blog"

cover_image: "/assets/images/projects/urldet-img.png"
live_url: "https://urldet.masahin.dev"

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