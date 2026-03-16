# Blood Cell Anomaly Detection

## Hakkında
Bu proje, tablo verileri kullanarak kan hücrelerindeki anomalileri tespit etmek amacıyla eğitilmiş bir makine öğrenmesi deneyidir. Temel veri ön işleme, özellik mühendisliği (feature engineering) ve Scikit-Learn ile model eğitimi süreçlerini pratik etmek için oluşturulmuştur. Hedef, bir kan hücresi örneğinin normal ("0") veya anormal ("1") olup olmadığını sınıflandırmaktır.

## Veri Seti
- **Kaynak:** `blood_cell_anomaly_detection.csv`
- **Boyut:** Veri seti; hücre morfolojisi özellikleri, kan ölçümleri, mikroskop bilgileri ve hasta verilerinden oluşmaktadır. (Model sızıntısını önlemek için `cytodiffusion_anomaly_score` gibi hedef etiketle doğrudan ilişkili sütunlar çıkarılmıştır.)

## Kurulum
```bash
pip install -r requirements.txt
jupyter notebook blood_cell_model.ipynb
```

## Sonuçlar
Projede ana model olarak `RandomForestClassifier` (max_depth=5, n_estimators=5) kullanılmıştır. Logistic Regression da test edilmiş ancak bu veri setinde Random Forest daha iyi sonuç vermiştir.

- **Doğruluk:** %97.5
- **F1-Score:** Belirtilmedi

## Geliştirici
YigitIbatBalta - @Destroyer307
