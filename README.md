# SVM ve K-Means ile Sınıflandırma Projesi

## Proje Hakkında

Bu projede, kediler ve köpekler arasında bir sınıflandırma yapılmıştır. Bunun için **Destek Vektör Makinesi (SVM)** ve **K-Means kümeleme** algoritmalarını kullandım. Veri seti, çeşitli boyutlardaki kedi ve köpek resimlerinden oluşuyordu. Bu resimleri işleyip standart boyutlara getirdikten sonra sınıflandırma işlemi için SVM'yi, verileri kümelere ayırmak için ise K-Means algoritmasını uyguladım.

Bu projede amacım, denetimli öğrenme (SVM) ile denetimsiz öğrenme (K-Means) arasındaki performans farklarını gözlemleyip bu algoritmaların hangi durumda daha etkili olduğunu öğrenmekti.

## Kullandığım Kütüphaneler

Projede veri işleme, görüntü işleme ve sınıflandırma yapmak için Python'un popüler kütüphanelerini kullandım:

- **NumPy**: Sayısal hesaplamalar ve dizi işlemleri için.
- **Pandas**: Verilerin düzenlenmesi ve analiz edilmesi için.
- **OS**: Dosya yollarını ve klasörleri yönetmek için.
- **Skimage**:
  - **imread**: Görselleri okuma.
  - **resize**: Görselleri yeniden boyutlandırma (150x150 piksel boyutuna getirdim).
- **Scikit-learn** (sklearn):
  - **SVC**: Destek Vektör Sınıflandırıcı (SVM).
  - **KMeans**: Verileri kümelere ayırmak için.
  - **StandardScaler**: Verileri ölçeklemek ve standartlaştırmak için.
  - **PCA**: Boyutları küçültmek ve veriyi daha iyi görselleştirmek için (K-Means ile kullanıldı).
- **Matplotlib**: Kümeleme sonuçlarını ve veri dağılımını grafikle göstermek için.
## Kullanılan Modeller

### 1. **Destek Vektör Makinesi (SVM)**

- **Çekirdek Fonksiyonu**: Doğrusal (linear) çekirdek kullanıldı.
- **Olasılık Tahminleri**: Sınıflandırma yaparken olasılık tahminleri (probability=True) kullanıldı.
- **Sonuçlar**:
  - **Doğruluk (Accuracy)**: %56.84
  - **Precision**: %56.97
  - **Recall**: %52.15
  - **F1 Skoru**: %54.45

SVM modeli, kediler ve köpekler arasında sınıflandırma yapmada ortalama bir performans sergiledi. Yüksek doğruluk oranı ve dengeli precision, recall ve F1 skoru değerleri sağladı, ancak bazı iyileştirmeler yaparak daha yüksek doğruluk ve diğer metrikleri elde edilebilir.

### 2. **K-Means Kümeleme**

- **Küme Sayısı**: 2 (Kediler ve Köpekler)
- **Boyut İndirgeme (PCA)**: Verinin görselleştirilmesi için kullanıldı.
- **Sonuçlar**:
  - **Doğruluk (Accuracy)**: %56.84
  - **Precision**: %56.97
  - **Recall**: %52.15
  - **F1 Skoru**: %54.45

K-Means, denetimsiz bir algoritma olarak veriyi iki kümeye ayırmayı başardı. Ancak, denetimsiz öğrenme algoritmalarının sınıflandırma doğruluğu genellikle daha düşük olabiliyor ve bu projede de sınıflandırma doğruluğu sınırlı kaldı.

## Performans Karşılaştırması

- **SVM**: Veriler üzerinde sınıflandırma yaparken daha yüksek doğruluk ve denge sağladı. Bu, etiketli veri kullanarak performansı daha yüksek olan bir denetimli öğrenme yöntemi olduğunu gösterdi.
- **K-Means**: K-Means kümeleme algoritması, etiketlenmemiş veri üzerinde çalıştığı için daha az başarılı sonuçlar verdi. Denetimsiz algoritmalar sınıflandırma görevlerinde sınırlı başarı sağlar.
## Sonuçlar

Bu projede, SVM gibi denetimli öğrenme yöntemlerinin, etiketli veri üzerinde daha iyi sonuçlar verdiğini gözlemledim. K-Means gibi denetimsiz öğrenme yöntemleri ise özellikle keşifsel analizler için yararlı olsa da, sınıflandırma görevlerinde SVM kadar başarılı değildi.

## Kaggle Not Defteri

Bu projeye ait Kaggle not defterine aşağıdaki bağlantıdan erişebilirsiniz:
(https://www.kaggle.com/code/lknurkoparir/classification-with-svm-kmeans/notebook)
