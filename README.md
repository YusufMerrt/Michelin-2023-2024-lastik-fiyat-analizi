# Lastik Maliyet Analizi Projesi

## 📊 Proje Özeti

# Start of Selection
Bu proje, lastik sektöründeki maliyet değişimlerini analiz eden ve gelecek dönem tahminlemeleri yapan bir veri bilimi çalışmasıdır. 2023-2024 yılları arasında 1814 farklı lastik ürününün maliyet verilerini inceleyerek, sektördeki fiyat dinamiklerini ve etkileyen faktörleri ortaya çıkarmaktadır. Ayrıca, Express Otomotiv ve [Tiryakiler Otomotiv](link) firmalarının gerçek Michelin lastik fiyat bilgileri de bu analizde yer almaktadır.

## 🎯 Amaç ve Kapsam
- Lastik maliyetlerindeki yıllık değişimlerin analizi
- Mevsimsel faktörlerin fiyatlandırmaya etkisinin incelenmesi
- Ebat bazlı maliyet farklılıklarının değerlendirilmesi
- Makine öğrenmesi ile maliyet tahmin modellerinin geliştirilmesi

Bu proje, lastik maliyetlerini analiz etmek için çeşitli veri bilimi tekniklerini kullanmaktadır. İlk olarak, veriler toplanmakta ve temizlenmektedir. Ardından, istatistiksel analizler ile verilerin temel özellikleri incelenmektedir. 

Makine öğrenmesi modelleri, geçmiş maliyet verilerini kullanarak gelecekteki maliyetleri tahmin etmek için eğitilmektedir. Lineer regresyon ve polinomial regresyon gibi modeller, maliyetlerin çeşitli değişkenlerle olan ilişkisini anlamak için kullanılmaktadır. Model performansı, Ortalama Kare Hata (MSE) ve R-kare (R²) gibi metriklerle değerlendirilmektedir. 

Sonuç olarak, bu proje, lastik maliyetlerindeki değişimleri anlamak ve gelecekteki fiyat tahminlerini yapmak için güçlü bir araç sunmaktadır.


## 📈 Önemli Bulgular

### Ortalama Fiyatlar
![alt text](image-2.png)

### Degiskenlerin korelasyonu
![alt text]({62919B35-4E1E-4FA4-879F-18A5514F4435}.png)



### Butun 2023 ve 2024 fiyatlarinin kiyaslanmasi
![alt text](image-3.png)


### Maliyet Değişim Analizi
- 2023'ten 2024'e ortalama maliyet artışı: %218
- En yüksek artış gösteren lastik kategorisi: kis


### Ebat Analizi Sonuçları
- Genişlik ve maliyet ilişkisi: 
![alt text](image.png)
- Yanak oranının fiyata etkisi: 
![alt text](image-1.png)



## 🤖 Makine Öğrenmesi Sonuçları

### Kullanılan Modeller ve Performansları

1. Lineer Regresyon
![alt text](image-4.png)
   Model Performans Metrikleri:
    - Ortalama Kare Hata (MSE): 787.24
    - R-kare (R²) Skoru: 0.99

    -Model Katsayıları:
    - Genişlik: 0.1770
    - Yanak: -0.2579
    - Maliyet 2023: -10.8103
    - inc: -15.7704
    - mevsim: 2.0107
    - Sabit (Intercept): 174.5347

2. Polinomial Regresyon
   ![alt text](image-5.png)
   Polynomial Regresyon Model Performans Metrikleri:
   - Ortalama Kare Hata (MSE): 736.64
   - R-kare (R²) Skoru: 0.99

3. Gradient Boosting Regresyon
![alt text](image-6.png)
   -    Gradient Boosting Regresyon Model Performans Metrikleri:
   - Ortalama Kare Hata (MSE): 903.32
   - R-kare (R²) Skoru: 0.99

4. Random Forest Regresyon
![alt text](image-7.png)
   -Random Forest Regresyon Model Performans Metrikleri:
   - Ortalama Kare Hata (MSE): 846.55
   - R-kare (R²) Skoru: 0.99

5. K-Means Kümeleme
![alt text](image-8.png)
K-Means Kümeleme Model Performans Metrikleri:
Küme Sayısı: 4
Küme Merkezleri:
- Küme 1: Düşük maliyetli, dar genişlik, düşük yanak oranı
- Küme 2: Orta maliyetli, geniş genişlik, orta yanak oranı
- Küme 3: Yüksek maliyetli, geniş genişlik, yüksek yanak oranı
- Küme 4: Çok yüksek maliyetli, dar genişlik, yüksek yanak oranı


### Model Karşılaştırması ve Seçimi
- En iyi performans: Gradient Boosting Regresyon
- Tercih sebebi: Yüksek doğruluk oranı ve özellik önem analizi kabiliyeti
- Cross-validation sonuçları: 5-fold CV ile %90 ortalama doğruluk



### Anomali Tespiti

- Local Outlier Factor ile bulunan anormal fiyatlamalar: 64 ürün
- Başlıca anomali nedenleri:
  - Mevsim dışı yüksek fiyatlamalar
  - Ebat-fiyat uyumsuzlukları
  - Beklenmeyen maliyet artışları

## 📋 Veri Seti Özellikleri
- Toplam ürün sayısı: 1814
- Zaman aralığı: 2023-2024
- Analiz edilen özellikler:
  - İnç (lastik çap ölçüsü)
  - Ebat (genişlik/yanak)
  - Mevsim
  - Maliyet bilgileri

## 💡 Öneriler ve Sonuçlar


1. Maliyet Optimizasyonu:
   - Doların sert hareketlerinin fiyatlandırmalara doğrudan etkisi bulunmaktadır. Özellikle maliyetlerin dolarla belirgin bir bağlantısı olduğu durumlarda, bu etkinin bazı modellere ve incelemelere göre daha fazla olacağı öngörülmektedir.
   - Maliyetlerin izlenmesi ve analiz edilmesi için düzenli raporlar oluşturulmalıdır.
   - Tedarik zinciri süreçlerinin optimize edilmesi, maliyetleri düşürebilir.
   - Farklı tedarikçilerle fiyat karşılaştırmaları yapılarak en uygun maliyetli seçenekler belirlenmelidir.
   

## 📚 Kullanılan Teknolojiler
- Python 3.x
- Pandas & NumPy: Veri analizi
- Scikit-learn: Makine öğrenmesi
- Matplotlib & Seaborn: Görselleştirme

## 👥 İletişim
- GitHub: [@kullaniciadi](https://github.com/kullaniciadi)
- LinkedIn: [LinkedIn Profiliniz](https://linkedin.com/in/kullaniciadi) #   M i c h e l i n - 2 0 2 3 - 2 0 2 4 - l a s t i k - f i y a t - a n a l i z i  
 