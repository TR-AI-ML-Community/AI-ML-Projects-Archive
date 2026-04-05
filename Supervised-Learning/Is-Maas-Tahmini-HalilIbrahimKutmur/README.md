# Is Maas Tahmini Projesi

## Hakkinda
Bu proje, makine ogrenmesi kullanarak calisanlarin kariyer ozellikleri (is pozisyonu, deneyim yili, egitim seviyesi, sektor, lokasyon vb.) uzerinden maas tahmini yapar. 

Projede farkli regresyon modelleri karsilastirilarak en yuksek performansi gosteren model belirlenmistir.

## Kullanilan Modeller
- **Linear Regression** (Baseline)
- **Random Forest Regressor**
- **Gradient Boosting Regressor**

## Veri Seti
- **Kaynak:** [Job Salary Prediction Dataset](https://www.kaggle.com/datasets)
- **Boyut:** 250,000 satir, 10 sutun
- **Hedef Degisken:** `salary` (Maas - USD)

### Ozellikler (Features)
| Ozellik | Aciklama | Tip |
|---------|----------|-----|
| `job_title` | Is unvani (AI Engineer, Data Analyst, vb.) | Kategorik |
| `experience_years` | Deneyim yili | Sayisal |
| `education_level` | Egitim seviyesi (High School, Bachelor, Master, PhD) | Kategorik |
| `skills_count` | Beceri sayisi | Sayisal |
| `industry` | Sektor (Healthcare, Telecom, Finance, vb.) | Kategorik |
| `company_size` | Sirket buyuklugu (Startup, Small, Medium, Large, Enterprise) | Kategorik |
| `location` | Lokasyon (USA, India, Germany, UK, vb.) | Kategorik |
| `remote_work` | Uzaktan calisma durumu (Yes, No, Hybrid) | Kategorik |
| `certifications` | Sertifika sayisi | Sayisal |

## Model Performansi

### Karsilastirma Tablosu

| Model | R2 (Egitim) | R2 (Test) | MAE ($) | RMSE ($) |
|-------|-------------|-----------|---------|----------|
| **Gradient Boosting** | 0.9768 | **0.9761** | **$4,583** | **$5,761** |
| Linear Regression | 0.9634 | 0.9635 | $5,436 | $7,126 |
| Random Forest | 0.9405 | 0.9314 | $7,672 | $9,766 |

### En Iyi Model: Gradient Boosting Regressor
- **R2 Score (Test):** 0.9761 (%97.61 aciklayicilik)
- **MAE (Ortalama Mutlak Hata):** $4,583
- **RMSE (Kok Ortalama Kare Hata):** $5,761

### Performans Yorumu
- **Gradient Boosting** en iyi performansi gostermistir. Test verisinde %97.61 aciklayicilik (R2) elde edilmistir.
- Ortalama tahmin hatasi (MAE) sadece $4,583'tir - bu maas tahminleri icin oldukca basarili bir sonuctur.
- Linear Regression de guclü performans gostermistir, bu veri setindeki iliskilerin buyuk olcude linear oldugunu gostermektedir.
- Random Forest overfitting egilimi gostermis ve test performansi dusuk kalmistir.

## Veri On Isleme
- **Kategorik veriler:** OneHotEncoder ile donusturuldu (LabelEncoder yerine daha uygun)
- **Sayisal veriler:** StandardScaler ile normalizasyon uygulandi
- **Pipeline:** ColumnTransformer ve Pipeline kullanilarak temiz bir is akisi olusturuldu

## Proje Yapisi
```
Is-Maas-Tahmini-HalilIbrahimKutmur/
├── data/
│   └── job_salary_prediction_dataset.csv
├── images/
│   ├── salary_distribution.png
│   ├── experience_vs_salary.png
│   ├── education_vs_salary.png
│   ├── job_title_salary.png
│   ├── correlation_heatmap.png
│   ├── model_comparison.png
│   ├── actual_vs_predicted.png
│   ├── residual_analysis.png
│   └── feature_importance.png
├── main.ipynb
├── README.md
└── requirements.txt
```

## Kurulum
Proje dosyalarini indirdikten sonra gerekli kutuphaneleri kurun:

```bash
pip install -r requirements.txt
```

## Calistirma
Jupyter Notebook'u baslatarak `main.ipynb` dosyasini acin:

```bash
jupyter notebook main.ipynb
```

## Onemli Bulgular
1. **Deneyim yili** maas uzerinde en etkili faktorlerden biridir
2. **Is unvani** (Machine Learning Engineer, Data Scientist vb.) maasi onemli olcude etkiler
3. **Egitim seviyesi** ve **lokasyon** da belirleyici faktorler arasindadir
4. **Sertifika sayisi** ve **beceri sayisi** nispeten daha az etkilidir

## Gelistirici
**Halil Ibrahim Kutmur** - [@halilibrahimkutmur](https://github.com/halilibrahimkutmur)
