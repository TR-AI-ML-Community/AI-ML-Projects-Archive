# Car Evaluation - Decision Tree

## Hakkında

Bu projede **car_evaluation.csv** veri seti kullanılarak araba değerlendirme sınıflandırması yapılmıştır.
Model olarak **Decision Tree Classifier** kullanılmıştır. Veri setindeki kategorik değişkenler **OrdinalEncoder** ile sayısal değerlere dönüştürülmüş ve modelin performansı test edilmiştir.

## Veri Seti

Projede **UCI Car Evaluation Dataset** kullanılmıştır.

Veri setinde bulunan başlıca özellikler:

* buying → araba satın alma maliyeti
* maint → bakım maliyeti
* doors → kapı sayısı
* persons → taşıma kapasitesi
* lug_boot → bagaj boyutu
* safety → güvenlik seviyesi

Hedef değişken:

* class → araba değerlendirme sonucu (unacc, acc, good, vgood)

## Kurulum

Projeyi çalıştırmak için gerekli Python kütüphanelerini yükleyin:

pip install -r requirements.txt

Gerekli kütüphaneler:

* pandas
* numpy
* scikit-learn
* matplotlib
* seaborn

## Sonuçlar

Decision Tree modeli ile yapılan sınıflandırma sonucunda model yaklaşık **%93.98 doğruluk oranı** elde etmiştir.

Model değerlendirmesi sırasında:

* veri train ve test olarak ayrılmıştır
* kategorik değişkenler encode edilmiştir
* Decision Tree Classifier modeli eğitilmiştir
* model doğruluğu test edilmiştir

## Geliştirici

Yiğit İbat Balta
