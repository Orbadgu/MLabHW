Manuel model, doğrusal regresyonun matematiksel temelini oluşturan normal denklemler (Normal Equation) yöntemiyle hazırlanmıştır. Bu yöntem, veri matrisine doğrudan matematiksel işlem uygulanarak ağırlıklar (θ değerleri) hesaplanır.

Sk-learn modeli, Python’un popüler makine öğrenmesi kütüphanesi olan sk-learn’de yer alan LinearRegression sınıfı ile eğitilmiştir. Bu model, arka planda optimize edilmiş yöntemlerle aynı doğrusal regresyon problemini çözer.

| Özellik                   | Manuel Model (NumPy) | Sk-learn Modeli      |
|---------------------------|----------------------|----------------------|
| Y-intercept (θ₀)          | 6.5956               | 6.5956               |
| Eğim Katsayısı (θ₁)       | 0.001531             | 0.001531             |
| Ortalama Kare Hata (MSE)  | 0.6119               | 0.6119               |

Her iki model de aynı regresyon doğrusunu üretmiştir. Bu, verilerin doğrusal yapısının iyi analiz edildiğini ve kullanılan yöntemlerin her ikisinin de doğru sonuçlar verdiğini göstermektedir.

Ortalama Kare Hata (MSE) değerlerinin birebir aynı olması, modellerin tahmin başarısında da fark olmadığını göstermektedir.

Manuel yöntem, algoritmanın mantığını anlamak açısından önemlidir; eğitim amaçlı projelerde faydalıdır. Ancak gerçek dünyada daha büyük ve karmaşık veri setleriyle çalışırken, sk-learn gibi optimize edilmiş kütüphaneler tercih edilmelidir.

Ayrıca sk-learn, model doğrulama, hiperparametre ayarı, çoklu değişkenli regresyon gibi ileri seviye işlemleri de desteklediğinden daha ölçeklenebilir ve esnek bir çözümdür.

Bu karşılaştırma, hem teorik hem de uygulamalı olarak doğrusal regresyon modellerinin nasıl çalıştığını göstermektedir. Manuel olarak yapılan hesaplamalarla scikit-learn çıktılarının birebir aynı olması, kullanılan araçlara olan güveni artırmakta ve doğru bir modelleme süreci izlendiğini teyit etmektedir.

KAYNAKÇA

https://www.kaggle.com/datasets/mariumfaheem666/top-rated-movies/data

https://www.geeksforgeeks.org/understanding-logistic-regression/

https://heena-sharma.medium.com/logistic-regression-python-implementation-from-scratch-without-using-sklearn-d3fca7d3dae7
