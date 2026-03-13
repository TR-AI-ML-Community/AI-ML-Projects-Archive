# MNIST-Digit-Classification-HalilIbrahimKutmur

## Hakkında
Bu proje, derin öğrenme (Deep Learning) kullanarak el yazısı rakamları sınıflandırır. **MNIST** veri seti üzerinde bir **Yapay Sinir Ağı (ANN)** modeli eğitilerek 0-9 arasındaki rakamların tanınması sağlanır.

Model, 28x28 piksellik gri tonlamalı görüntüleri girdi olarak alır ve Flatten → Dense(50, ReLU) → Dense(50, ReLU) → Dense(10, Sigmoid) katmanlarından oluşan bir mimari ile sınıflandırma yapar.

## Veri Seti
- **Kaynak:** [MNIST Handwritten Digits](http://yann.lecun.com/exdb/mnist/) (Keras üzerinden otomatik indirilir)
- **Boyut:** 70.000 görüntü (60.000 eğitim + 10.000 test), 28x28 piksel
- **Sınıflar:** 0-9 arası 10 rakam

## Kullanılan Teknolojiler
- **Python**: Veri analizi ve modelleme
- **NumPy**: Sayısal işlemler ve veri manipülasyonu
- **Matplotlib & Seaborn**: Veri görselleştirme ve Confusion Matrix
- **TensorFlow / Keras**: Yapay sinir ağı modeli oluşturma ve eğitme

## Proje Adımları
1. **Veri Yükleme:** MNIST veri setinin Keras üzerinden yüklenmesi.
2. **Veri Keşfi:** Görüntü boyutları, etiket dağılımı ve örnek görsellerin incelenmesi.
3. **Ön İşleme:** Piksel değerlerinin 0-1 arasına normalize edilmesi (/ 255).
4. **Model Oluşturma:** Sequential model ile ANN mimarisinin kurulması.
5. **Eğitim:** Adam optimizer ve sparse_categorical_crossentropy loss ile 10 epoch eğitim.
6. **Değerlendirme:** Test seti üzerinde doğruluk hesaplama ve Confusion Matrix görselleştirmesi.

## Sonuçlar
- **Test Doğruluğu (Accuracy):** %96.43
- **Test Loss:** 0.149

## Kurulum
Proje dosyalarını indirdikten sonra gerekli kütüphaneleri kurun:

```bash
pip install -r requirements.txt
```

## Geliştirici
**Halil İbrahim Kutmur** - [@HalilIbrahimKutmur](https://github.com/HalilIbrahimKutmur)