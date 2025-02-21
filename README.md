# **Telco Müşteri Kaybı (Churn) Tahmini**


---

## **Amaç**
Bu projenin amacı, bir telekomünikasyon şirketinin müşteri verilerini kullanarak, hangi müşterilerin hizmetlerden ayrılma (**churn**) eğiliminde olduğunu tahmin etmektir. Bu tahminler sayesinde şirket, müşteri kaybını önlemek için proaktif adımlar atabilir ve müşteri memnuniyetini artırabilir.

---

## **Problem Tanımı**
Telekomünikasyon sektöründe müşteri kaybı (**churn**), şirketler için önemli bir sorundur. Müşterilerin hizmetlerden ayrılması, şirketin gelir kaybına ve müşteri tabanının azalmasına neden olur.

Bu projede:
- Mevcut müşteri verileri analiz edilecek,
- Hangi müşterilerin churn olma olasılığının yüksek olduğu belirlenecek,
- Bu müşterilere yönelik özel kampanyalar veya teklifler sunulması hedeflenmektedir.

Veri seti, müşteri kimlik numarası, demografik bilgiler, hizmet kullanım detayları, sözleşme bilgileri ve churn durumu gibi çeşitli özellikler içermektedir. Bu veriler kullanılarak churn tahmini yapmak için makine öğrenimi modelleri geliştirilecektir.

---
### **Veri Setinin Seçimi ve Hazırlanması**

#### **Veri Seti:**
- **Kaynak:** [Kaggle - Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- **Boyut:** 7043 satır, 21 sütun
- **Hedef Değişken:** `Churn` (Müşterinin churn olup olmadığı)

#### **Veri Seti Özellikleri:**
**Demografik Bilgiler:**
  - Cinsiyet (`gender`)
  - Yaşlılık durumu (`SeniorCitizen`)
  - Eş varlığı (`Partner`)
  - Bağımlılar (`Dependents`)

**Hizmet Bilgileri:**
  - Telefon hizmeti (`PhoneService`)
  - Çoklu hat (`MultipleLines`)
  - İnternet servisi (`InternetService`)
  - Çevrimiçi güvenlik (`OnlineSecurity`)
  - Yedekleme (`OnlineBackup`)
  - Cihaz koruma (`DeviceProtection`)
  - Teknik destek (`TechSupport`)
  - TV ve film akışı (`StreamingTV`, `StreamingMovies`)

**Müşteri Bilgileri:**
  - Kontrat süresi (`Contract`)
  - Fatura yöntemi (`PaperlessBilling`)
  - Ödeme yöntemi (`PaymentMethod`)
  - Aylık ücret (`MonthlyCharges`)
  - Toplam ücret (`TotalCharges`)
  - Müşteri süresi (`tenure`)
    
---

## **Kullanılan Yöntemler ve Araçlar**

### **1. Veri Analizi ve Görselleştirme**
- **Python kütüphaneleri:** Pandas, NumPy, Matplotlib, Seaborn
- Eksik veriler, aykırı değerler ve kategorik değişkenlerin analizi yapılacaktır.
- Veri dağılımları ve ilişkileri görselleştirilecektir.

### **2. Veri Ön İşleme**
- Kategorik değişkenlerin kodlanması: **One-Hot Encoding**, **Label Encoding**
- Veri normalizasyonu ve ölçeklendirme
- Veri setinin eğitim ve test setlerine ayrılması

### **3. Makine Öğrenmesi Modelleri**
Aşağıdaki sınıflandırma modelleri kullanılacaktır:
- Lojistik Regresyon
- Karar Ağaçları
- Random Forest
- Gradient Boosting
- XGBoost

Model performansı aşağıdaki metriklerle değerlendirilecektir:
- Doğruluk (**Accuracy**)
- Kesinlik (**Precision**)
- Duyarlılık (**Recall**)
- F1 Skoru

### **4. Model Optimizasyonu**
- Hiperparametre optimizasyonu: **Grid Search**, **Random Search**
- Özellik mühendisliği ve özellik seçimi ile model performansı artırılacaktır.

### **5. Araçlar**
- **Programlama Dili:** Python
- **Çalışma Ortamı:** Google Colab, Kaggle Notebook
- **Kütüphaneler:** Scikit-learn, XGBoost, Pandas, NumPy, Matplotlib, Seaborn

---

## **Sonuçlar**
Veri seti üzerinde yapılan analizler ve modellemeler sonucunda:
- Churn tahmini yapmak için en iyi performans gösteren model belirlenecektir.
- Modelin doğruluk oranı, churn olan müşterileri doğru bir şekilde tahmin etme yeteneği ve diğer performans metrikleri raporlanacaktır.

Şirket, bu model sayesinde churn riski yüksek olan müşterileri belirleyebilecek ve bu müşterilere yönelik özel kampanyalar düzenleyebilecektir.

---

## **Gelecek Planlamaları (Opsiyonel)**

### **1. Model Geliştirme**
- Daha fazla veri toplanarak modelin genelleme yeteneği artırılabilir.
- Derin öğrenme modelleri (örneğin, sinir ağları) kullanılarak model performansı daha da iyileştirilebilir.

### **2. Otomatikleştirme**
- Model, şirketin CRM sistemine entegre edilerek gerçek zamanlı churn tahminleri yapılabilir.
- Otomatik raporlama ve uyarı sistemleri geliştirilebilir.

### **3. Müşteri Segmentasyonu**
- Churn riski yüksek olan müşteriler, demografik ve davranışsal özelliklerine göre segmentlere ayrılabilir.
- Segmentlere göre kişiselleştirilmiş kampanyalar sunulabilir.

---

> **Not:** Bu proje, telekomünikasyon şirketlerinin müşteri kaybını minimize etmek ve müşteri memnuniyetini artırmak için stratejik kararlar almasına yardımcı olacaktır.
