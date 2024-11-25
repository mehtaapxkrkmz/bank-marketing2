# Bank Marketing Prediction with Decision Tree

**Kullanılan Dataset**: [Bank Marketing Dataset](https://www.kaggle.com/datasets/janiobachmann/bank-marketing-dataset)

Bu proje, bir bankanın müşteri verilerini kullanarak, müşterilerin bir bankanın ürününü satın alıp almayacağını tahmin etmeyi amaçlamaktadır. Karar ağacı algoritması kullanılarak bu tahminler yapılmış ve modelin doğruluğu, karmaşıklığı, doğruluk oranı (accuracy) ve konfizyon matrisi gibi değerlendirme metrikleri hesaplanmıştır.

## İçindekiler

- [Proje Hakkında](#proje-hakkında)
- [Veri Seti](#veri-seti)
- [Modelin Eğitilmesi ve Değerlendirilmesi](#modelin-eğitilmesi-ve-değerlendirilmesi)
- [Kullanılan Kütüphaneler](#kullanılan-kütüphaneler)
- [Sonuçlar](#sonuçlar)
- [Sonuçlar ve Değerlendirme](#sonuçlar-ve-değerlendirme)
- [Yapılacaklar](#yapılacaklar)

## Proje Hakkında

Bu projede, bank marketing kampanyasına katılan müşterilerin bilgileri kullanılarak, müşterilerin bir bankanın ürününü satın alıp almayacağı tahmin edilmiştir. Proje, sınıflandırma problemi olup, hedef değişken "deposit" (evet veya hayır) olup, modelin başarısını değerlendirmek için karar ağacı (decision tree) algoritması kullanılmıştır.

## Veri Seti

Veri seti, bir bankanın müşterilerinin demografik ve geçmiş finansal bilgilerini içermektedir. Her müşteri için aşağıdaki özellikler mevcuttur:

- **Age**: Yaş
- **Job**: İş türü
- **Marital**: Medeni durum
- **Education**: Eğitim durumu
- **Balance**: Hesap bakiyesi
- **Housing**: Konut kredisi var mı
- **Loan**: Kredi kartı borcu var mı
- **Contact**: İletişim kanalı
- **Previous**: Önceki kampanyaya katılım durumu
- **Campaign**: Kampanyaya katılım sayısı
- **Pdays**: Sonraki kampanya için gün sayısı
- **Duration**: İletişim süresi
- **Y**: Hedef değişken (1: Ürünü satın aldı, 0: Satın almadı)

## Modelin Eğitilmesi ve Değerlendirilmesi

1. **Veri Setinin Hazırlanması**: Veri seti, eğitim ve test verilerine ayrılmıştır. Eğitim verisi ile model eğitilmiş ve test verisi ile değerlendirilmiştir.
   
2. **Öznitelik Dönüşümü**: Kategorik veriler, one-hot encoding yöntemi ile sayısal verilere dönüştürülmüştür.
   
3. **Modelin Eğitilmesi**: Karar ağacı (decision tree) algoritması kullanılarak eğitim verisi üzerinde model eğitilmiştir.
   
4. **Model Değerlendirmesi**:
   - **Doğruluk Oranı (Accuracy)**: Modelin doğru tahminlerinin oranı hesaplanmıştır.
   - **Confusion Matrix**: Modelin sınıflandırma başarısını görselleştiren bir karmaşıklık matrisi oluşturulmuştur.

## Kullanılan Kütüphaneler

Proje için aşağıdaki Python kütüphaneleri kullanılmıştır:

- `pandas` - Veri işleme ve manipülasyonu için
- `numpy` - Matematiksel hesaplamalar için
- `scikit-learn` - Model eğitimi, test ve değerlendirme metrikleri için
- `matplotlib` ve `seaborn` - Veri görselleştirme için

## Sonuçlar

- **Accuracy**: Modelin doğruluk oranı, eğitim ve test verisi üzerinde hesaplanmıştır.
- **Confusion Matrix**: Modelin doğru ve yanlış tahminlerini görsel olarak sunan bir konfizyon matrisi oluşturulmuştur.

Örnek:

- **Confusion Matrix**:
 [[True Negatives, False Positives] [False Negatives, True Positives]]


- **Accuracy**: Modelin test verisi üzerindeki doğruluk oranı hesaplanmıştır.

## Sonuçlar ve Değerlendirme

Model, genel olarak iyi bir performans göstermiştir.Modelin geliştirilmesi için bazı iyileştirmeler yapılabilir. Örneğin:

- Veri temizliği ve ön işleme süreçleri geliştirilerek modelin doğruluğu artırılabilir.
- Daha karmaşık modeller, örneğin rastgele orman (random forest) veya destek vektör makineleri (SVM), denenebilir.
- Kategorik veriler için farklı dönüştürme teknikleri kullanılabilir.

## Yapılacaklar

1. Modelin başarısını artırmak için hyperparametre optimizasyonu yapılabilir.
2. Modelin doğruluğunu artırmak için daha fazla veri eklenebilir.
3. Farklı sınıflandırma algoritmaları ile karşılaştırma yapılabilir.

