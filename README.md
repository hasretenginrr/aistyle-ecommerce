# AIStyle — Personalized E-Commerce Recommendation System

[English](#overview) | [Türkçe](#türkçe)

## Overview

AIStyle is described in the original project documentation as a web-based e-commerce application that recommends products based on a user's purchase history. It combines product browsing and order management with content-based recommendations.

> **Repository status:** The inspected `main` branch contains only this README. Source code, datasets, database migrations, and setup scripts are not included. The implementation details below preserve the original project description; they have not been verified against source code or a running application.

<img width="1875" height="897" alt="Ekran görüntüsü 2025-06-02 144113" src="https://github.com/user-attachments/assets/b26c13ca-0a91-4c75-a146-b9605e6b8b61" />

<img width="1192" height="522" alt="Ekran görüntüsü 2025-06-02 144548" src="https://github.com/user-attachments/assets/3a893c5c-ca75-4bb9-8713-29e388caf4b8" />
<img width="1861" height="868" alt="Ekran görüntüsü 2025-06-02 144445" src="https://github.com/user-attachments/assets/8bcf10ff-178d-4df0-8f7e-5768f18b6b0c" />

<img width="1878" height="850" alt="Ekran görüntüsü 2025-06-02 145036" src="https://github.com/user-attachments/assets/a0e1f1e7-f6fb-4466-b398-dbc5b766ff2c" />
<img width="1557" height="474" alt="Ekran görüntüsü 2025-06-02 145221" src="https://github.com/user-attachments/assets/34190837-75f7-420c-98b2-4023f19ce133" />
<img width="1452" height="824" alt="Ekran görüntüsü 2025-06-02 145230" src="https://github.com/user-attachments/assets/a21c6e19-093a-41ce-b3bf-07c8d64619ec" />
<img width="1400" height="803" alt="Ekran görüntüsü 2025-06-14 184333" src="https://github.com/user-attachments/assets/27d36beb-6af7-41ce-86ed-08905752c7f0" />





## Project Scope

The original documentation describes:

- User management.
- A categorized product catalog.
- Order processing.
- Personalized product recommendations based on previous purchases.
- A Turkish storefront adapted from an HTML/CSS template.

## Technology Stack

| Technology | Described role |
| --- | --- |
| C# / ASP.NET Core MVC | Application backend, controllers, and views |
| Entity Framework Core | Data access |
| PostgreSQL | Relational database |
| ML.NET | Text-based product recommendation pipeline |
| Python / Pandas / NumPy | Dataset cleaning and preprocessing |
| Google Translate API | Product-content translation |
| HTML / CSS template | Storefront presentation adapted to MVC |

The application is described as using a layered architecture. Exact project boundaries, package versions, and runtime requirements are not available in this repository.

## Dataset Preparation

The original project description reports a catalog of **14,041 products** after preprocessing the Myntra dataset.

The described preparation steps were:

1. Clean missing and incorrect data with Pandas and NumPy.
2. Translate product information in batches using the Google Translate API.
3. Adapt column names and product descriptions for a Turkish-language storefront.
4. Use the prepared data in the e-commerce application.

The dataset, preprocessing scripts, source dataset link, and licensing details are not included here. Review the applicable dataset and template licenses before redistributing their contents.

## Recommendation Approach

The documented approach is **content-based recommendation**, using product attributes rather than describing a collaborative-filtering or generative-AI system.

1. Use previously purchased products as recommendation input.
2. Analyze product names, descriptions, and colors.
3. Convert text into numerical features using TF-IDF in an ML.NET pipeline.
4. Calculate cosine similarity between product representations.
5. Suggest products with similar content.

The repository does not specify how multiple past purchases are combined, whether purchased products are excluded, or how recommendations are evaluated. No recommendation-quality metrics are provided.

## Repository Contents and Setup

Only `README.md` is currently present on the inspected `main` branch.

The project cannot be built or run from this repository alone. A reproducible setup would require:

- Application source code and solution/project files.
- .NET and dependency versions.
- Database schema or migrations.
- Sanitized configuration examples without credentials.
- Dataset source and preparation/import instructions.
- Any required ML artifacts or instructions to generate them.
- Build, run, and test instructions.

No installation commands are provided because the required files and configuration are not available.

## Türkçe

### Proje Hakkında

AIStyle, özgün proje açıklamasına göre kullanıcıların geçmiş alışverişlerini analiz ederek benzer ürünler öneren, web tabanlı bir e-ticaret uygulamasıdır. Ürün listeleme ve sipariş işlemlerini içerik tabanlı kişiselleştirilmiş önerilerle birleştirir.

> **Depo durumu:** İncelenen `main` dalında yalnızca bu README bulunmaktadır. Kaynak kodlar, veri seti, veritabanı migration dosyaları ve kurulum betikleri eklenmemiştir. Aşağıdaki bilgiler özgün proje açıklamasına dayanır; kaynak kod veya çalışan uygulama üzerinden doğrulanmamıştır.

### Proje Kapsamı

- Kullanıcı yönetimi.
- Kategorilere ayrılmış ürün kataloğu.
- Sipariş işlemleri.
- Önceki satın alımlara göre kişiselleştirilmiş ürün önerileri.
- HTML/CSS şablonunun MVC yapısına uyarlanmasıyla oluşturulmuş Türkçe arayüz.

### Kullanılan Teknolojiler

| Teknoloji | Açıklanan kullanım amacı |
| --- | --- |
| C# / ASP.NET Core MVC | Backend, controller ve view yapıları |
| Entity Framework Core | Veri erişimi |
| PostgreSQL | Veritabanı |
| ML.NET | Metin tabanlı ürün önerileri |
| Python / Pandas / NumPy | Veri temizleme ve ön işleme |
| Google Translate API | Ürün bilgilerinin çevirisi |
| HTML / CSS şablonu | E-ticaret arayüzü |

Özgün açıklamada katmanlı mimari kullanıldığı belirtilmektedir. Proje katmanlarının dosya yapısı, paket sürümleri ve çalışma ortamı gereksinimleri depoda bulunmamaktadır.

### Veri Setinin Hazırlanması

Özgün proje açıklamasına göre Myntra veri seti, Pandas ve NumPy ile eksik ve hatalı verilerden temizlenmiş; sonuçta **14.041 ürünlük** bir katalog elde edilmiştir.

Ürün bilgileri Google Translate API ile parçalar hâlinde çevrilmiş, sütun adları ve açıklamalar Türkçe platforma uyarlanmıştır.

Veri seti, ön işleme kodları, kaynak veri setinin bağlantısı ve lisans bilgileri depoda yer almamaktadır. Veri seti veya şablon dosyaları paylaşılmadan önce ilgili lisans koşulları kontrol edilmelidir.

### Öneri Sistemi

Açıklanan yöntem **içerik tabanlı filtrelemedir**:

1. Kullanıcının önceki satın alımları temel alınır.
2. Ürünlerin ad, açıklama ve renk özellikleri değerlendirilir.
3. ML.NET üzerinde TF-IDF ile metinler sayısal özelliklere dönüştürülür.
4. Ürünler arasında kosinüs benzerliği hesaplanır.
5. Benzer içerikli ürünler kullanıcıya önerilir.

Birden fazla satın alımın nasıl birleştirildiği, daha önce alınan ürünlerin önerilerden çıkarılıp çıkarılmadığı ve öneri kalitesinin nasıl ölçüldüğü mevcut açıklamada belirtilmemiştir. Performans metriği paylaşılmamıştır.

### Kurulum ve Çalıştırma

Depoda yalnızca README bulunduğundan uygulama bu depodan tek başına çalıştırılamaz.

Tekrarlanabilir bir kurulum için kaynak kodların, solution/proje dosyalarının, sürüm bilgilerinin, veritabanı şeması veya migration dosyalarının, gizli bilgi içermeyen yapılandırma örneklerinin ve veri hazırlama adımlarının eklenmesi gerekir.

Bu dokümantasyon güncellemesinde uygulama çalıştırılmamış, derleme veya test yapılmamıştır.
