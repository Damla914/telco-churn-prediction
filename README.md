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

--- Model Comparisİon Table ---
                 Model  Accuracy  Precision    Recall  F1-Score   AUC-ROC
0  Logistic Regression  0.751955   0.527115  0.649733  0.582036  0.719348
1        Random Forest  0.780384   0.579853  0.631016  0.604353  0.732739
2             LightGBM  0.772566   0.564286  0.633690  0.596977  0.728268

## Sonuç

Analizler sonucunda genel performansı ve tahmin tutarlılığı en yüksek olan Random Forest modeli, nihai tahmin modeli olarak seçilmiştir.