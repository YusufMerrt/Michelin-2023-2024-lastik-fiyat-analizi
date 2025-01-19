# Lastik Veri Analizi - Ürün Gereksinimleri Belgesi (PRD)

## 1. Ürün Özeti
Bu proje, lastik verilerinin analizi ve görselleştirilmesi için bir veri analizi çözümüdür. Sistem, lastik özelliklerini analiz ederek fiyatlandırma ve stok yönetimi konularında içgörüler sağlamayı amaçlamaktadır. 2023-2024 yılları arasındaki maliyet değişimlerini ve mevsimsel faktörlerin etkisini makine öğrenmesi yöntemleriyle incelemektedir.

## 2. Problem Tanımı ve Hedefler
### 2.1 Ana Problemler
- Farklı lastik ebatları ve özellikleri için maliyet analizinin yapılması
- Mevsimsel faktörlerin lastik maliyetlerine etkisinin anlaşılması
- 2023-2024 maliyet karşılaştırmalarının yapılması

### 2.2 Hedefler
- Maliyet artışlarının kategorilere göre analizi
- Mevsimsel stok planlaması için öngörü oluşturma
- Ebat bazlı maliyet optimizasyonu önerileri

## 3. Veri Özellikleri ve Yapısı
### 3.1 Ana Veri Alanları
- İnç (inc): Lastik çap ölçüsü
- Kod: Ürün tanımlama kodu
- Ebat: Genişlik ve yanak bilgisi
- Mevsim: Kullanım mevsimi
- 2023 KDV Dahil Maliyet
- 2024 KDV Dahil Maliyet

### 3.2 Veri Kaynakları
- Express Ocak 2024 Maliyet Tablosu
- 2023 yılı maliyet verileri
- Toplam 1814 ortak ürün verisi

## 4. Fonksiyonel Gereksinimler
### 4.1 Veri İşleme
- Ebat verilerinin genişlik ve yanak olarak ayrıştırılması
- Gereksiz sütunların temizlenmesi
- Veri tiplerinin uygun formata dönüştürülmesi
- Eksik verilerin temizlenmesi

### 4.2 Analiz Gereksinimleri
- Mevsimsel maliyet analizi
- Ebat bazlı maliyet karşılaştırması
- Yıllık maliyet değişimi analizi
- İstatistiksel analizler ve trend tespiti
- Makine öğrenmesi modelleri ile maliyet tahminleri

### 4.3 Makine Öğrenmesi Analizleri
- Regresyon modelleri ile maliyet tahminleri
- Kümeleme analizi ile lastik gruplarının belirlenmesi
- Özellik önem analizi ile maliyet etkenleri
- Model performans değerlendirmesi ve doğrulama

## 5. Teknik Gereksinimler
### 5.1 Kullanılan Teknolojiler
- Python 3.x
- Pandas: Veri manipülasyonu için
- Matplotlib ve Seaborn: Veri görselleştirme için
- Jupyter Notebook: Geliştirme ortamı
- Scikit-learn: Makine öğrenmesi modelleri için
- NumPy: Sayısal işlemler için

### 5.2 Veri İşleme Gereksinimleri
- Excel dosyalarının otomatik işlenmesi
- Veri temizleme ve dönüştürme işlemleri
- Görselleştirme ve raporlama araçları

## 6. Analiz ve Bulgular

### 6.1 Maliyet Değişim Analizi
- 2023'ten 2024'e maliyet artış oranları
- Kategorilere göre maliyet değişimleri
- Mevsimsel etkilerin maliyete yansıması

### 6.2 Ebat Analizi
- Genişlik ve yanak oranlarının maliyet üzerindeki etkisi
- En çok maliyet artışı gösteren ebatlar
- Optimum stok planlaması için ebat bazlı öneriler

### 6.3 Mevsimsel Analiz
- Mevsim bazında maliyet farklılıkları
- Stok rotasyonu önerileri
- Mevsimsel talep tahminleri

### 6.4 Makine Öğrenmesi Analiz Sonuçları
- Regresyon modellerinin tahmin performansı
- Önemli maliyet belirleyici faktörler
- Lastik grupları ve karakteristikleri
- Model doğruluk metrikleri ve güven aralıkları
- Anomali tespiti ve özel durumlar

## 7. Başarı Kriterleri
### 7.1 Teknik Kriterler
- Veri temizleme ve dönüştürme işlemlerinin doğruluğu
- Analiz sonuçlarının tutarlılığı
- Raporların anlaşılabilirliği
- Makine öğrenmesi modellerinin performansı (R², MAE, RMSE)
- Tahmin doğruluğu ve güvenilirliği

### 7.2 İş Kriterleri
- Maliyet optimizasyonu önerilerinin uygulanabilirliği
- Stok yönetimi verimliliğinde artış
- Mevsimsel planlamanın doğruluğu

## 8. Proje Zaman Çizelgesi
### 8.1 Fazlar
1. Veri Hazırlama ve Temizleme: 1 hafta
   - Veri kaynaklarının birleştirilmesi
   - Veri temizleme ve dönüştürme
   
2. Analiz ve Görselleştirme: 2 hafta
   - İstatistiksel analizler
   - Görsel raporların hazırlanması
   
3. Raporlama ve Dokümantasyon: 1 hafta
   - Sonuçların dokümantasyonu
   - Önerilerin hazırlanması

## 9. Riskler ve Kısıtlamalar
### 9.1 Teknik Riskler
- Veri kalitesi ve tutarlılığı
- Eksik veri noktaları
- Sistem performans kısıtlamaları

### 9.2 İş Riskleri
- Mevsimsel değişimlerin düzensizliği
- Pazar koşullarındaki beklenmedik değişimler
- Tedarik zinciri aksaklıkları

## 10. Teknik Kazanımlar ve Gelişim
### 10.1 Proje Sürecindeki Teknik Kazanımlar
#### Veri Bilimi ve Analitik
- Python ile büyük veri setlerinin işlenmesi ve analizi
- Pandas kütüphanesi ile veri manipülasyonu ve temizleme
- Matplotlib ve Seaborn ile ileri düzey veri görselleştirme
- Scikit-learn ile makine öğrenmesi modellerinin geliştirilmesi

#### Veri Ön İşleme
- Eksik veri yönetimi ve temizleme teknikleri
- Veri normalizasyonu ve standardizasyonu
- Kategorik veri dönüşümleri
- Özellik mühendisliği ve seçimi

#### Makine Öğrenmesi
- Regresyon modellerinin uygulanması ve optimizasyonu
- Kümeleme algoritmaları ile veri segmentasyonu
- Model performans değerlendirme ve doğrulama
- Hiperparametre optimizasyonu

#### Yazılım Geliştirme
- Git ile versiyon kontrolü
- Jupyter Notebook ile interaktif geliştirme
- Modüler kod yapısı oluşturma
- Kod dokümantasyonu ve yorum yazımı

### 10.2 Gelecek Hedefler ve Geliştirmeler
#### Teknik Hedefler
- Derin öğrenme modellerinin uygulanması
- Otomatik model güncelleme sisteminin kurulması
- API entegrasyonu ile gerçek zamanlı veri akışı


#### Analitik Hedefler
- Zaman serisi analizi ile trend tahminleri
- Anomali tespiti sistemlerinin geliştirilmesi
- Çok değişkenli analiz teknikleri
- İleri seviye istatistiksel modelleme


### 10.3 Profesyonel Gelişim Planı
#### Kısa Vadeli (0-6 ay)
- İleri seviye Python programlama
- Makine öğrenmesi algoritmalarında uzmanlaşma
- Veri görselleştirme tekniklerinin geliştirilmesi


#### Orta Vadeli (6-12 ay)
- Derin öğrenme framework'lerinin öğrenilmesi
- Bulut platformlarında uzmanlık (AWS/Azure)
- DevOps pratiklerinin benimsenmesi
- Büyük veri teknolojilerinin öğrenilmesi

#### Uzun Vadeli (12+ ay)
- MLOps süreçlerinin kurulması
- Veri bilimi ekip liderliği
- Endüstri standartlarını belirleme
- Açık kaynak projelere katkı 