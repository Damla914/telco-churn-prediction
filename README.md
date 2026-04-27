## Telco Customer Churn Prediction (Müşteri Kayıp Tahmini)

Bu proje, bir telekomünikasyon şirketinin müşteri verilerini analiz ederek, hangi müşterilerin hizmeti terk etme (churn) eğiliminde olduğunu önceden tahmin etmeyi amaçlar. Proje kapsamında veri temizleme, özellik mühendisliği, sınıflandırma modelleri ve iş stratejisi geliştirme adımları uygulanmıştır.


### Proje Özeti
 
Yeni bir müşteri kazanmanın maliyeti, mevcut müşteriyi elde tutmaktan çok daha yüksektir. Bu projede geliştirilen makine öğrenmesi modelleriyle, yüksek riskli müşteriler tespit edilerek şirketin proaktif önlemler alması hedeflenmektedir.


### Kullanılan Teknolojiler

Python 
Pandas & NumPy: Veri manipülasyonu ve analizi.
Matplotlib & Seaborn: Veri görselleştirme.
Scikit-Learn: Makine öğrenmesi modelleri ve metrikler.
Imbalanced-Learn (SMOTE): Sınıf dengesizliğini giderme.
LightGBM: Yüksek performanslı gradient boosting modeli.


### Veri Seti ve Özellik Mühendisliği

Projede kullanılan Telco Customer Churn veri seti üzerinde aşağıdaki Feature Engineering çalışmaları yapılmıştır:
  AverageMonthlyCharge: Müşterinin toplam harcamasının kullanım süresine oranı.
  IsNewCustomer: 12 aydan kısa süreli müşterilerin tespiti.
  NoSupportRisk: Teknik destek ve online güvenlik hizmeti almayan riskli grup tanımlaması.
  HighRiskContract: Aylık (Month-to-month) sözleşme sahiplerinin belirlenmesi.
  
### Modelleme ve Performans

Veri setindeki sınıf dengesizliği (imbalance) SMOTE tekniği ile giderilmiştir. Üç farklı model karşılaştırılmıştır:

| Model | Accuracy | Precision | Recall | F1-Score | AUC-ROC |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Random Forest** | 0.780 | 0.579 | 0.631 | **0.604** | **0.732** |
| LightGBM | 0.772 | 0.564 | 0.633 | 0.596 | 0.728 |
| Logistic Regression | 0.751 | 0.527 | **0.649** | 0.582 | 0.719 |

## Sonuç

Analizler sonucunda genel performansı ve tahmin tutarlılığı en yüksek olan Random Forest modeli, nihai tahmin modeli olarak seçilmiştir.
