# Student-Dropout-Prediction-HalilIbrahimKutmur

## Hakkında
Bu proje, makine öğrenmesi (Logistic Regression) kullanarak üniversite öğrencilerinin okuldan ayrılma (dropout) riskini tahmin eder. Model; yaş, GPA, devamsızlık oranı, çalışma saatleri, stres endeksi, aile geliri ve burs durumu gibi 17 farklı özelliği analiz ederek ikili sınıflandırma (ayrılacak/kalacak) yapar.

## Veri Seti
- **Kaynak:** Student Dropout Dataset (`student_dropout_dataset_v3.csv`)
- **Boyut:** 10.000 satır, 19 özellik (Age, Gender, Family_Income, Internet_Access, Study_Hours_per_Day, Attendance_Rate, Assignment_Delay_Days, Travel_Time_Minutes, Part_Time_Job, Scholarship, Stress_Index, GPA, Semester_GPA, CGPA, Semester, Department, Parental_Education, Dropout)

## Kurulum
Proje dosyalarını indirdikten sonra gerekli kütüphaneleri kurmak için aşağıdaki komutu çalıştırın:

```bash
pip install -r requirements.txt
```

## Sonuçlar
- **Doğruluk (Train):** %80.93
- **Doğruluk (Test):** %81.30
- **F1-Score:** 0.50

## Geliştirici
**Halil İbrahim Kutmur** - [@github](https://github.com/HalilIbrahimKutmur)
