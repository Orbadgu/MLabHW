Veri setinde yer alan şaraplara ait çeşitli kimyasal özellikler kullanılarak, şarap kalitesinin “iyi” (kalite ≥ 6) veya “kötü” (kalite < 6) olarak sınıflandırılması hedeflenmiştir. Bu amaçla quality sütunu ikili hale getirilmiş ve sınıflandırma problemi oluşturulmuştur.

Veri, eğitim ve test olmak üzere %80-%20 oranında bölünmüş, ardından değişkenler standartlaştırılarak modele uygun hale getirilmiştir. Sinir ağı modeli tek gizli katmanlı olarak tasarlanmıştır: giriş katmanında özellik sayısı kadar nöron, gizli katmanda 10 nöron ve çıkış katmanında bir adet sigmoid aktivasyonlu nöron yer almaktadır. Gizli katmanda ReLU aktivasyonu tercih edilmiştir. Model, forward ve backward propagation algoritmalarıyla 1000 epoch boyunca eğitilmiştir. Her 100 epoch’ta bir loss değeri yazdırılmış, böylece öğrenme süreci izlenmiştir. Modelin başarımı, test verileri üzerinde yapılan tahminlerle ölçülmüş ve doğruluk değeri hesaplanmıştır.
|                 | Gerçek Pozitif (1) | Gerçek Negatif (0) |
|-----------------|--------------------|---------------------|
| Tahmin: 1       | TP = 252           | FP = 70             |
| Tahmin: 0       | FN = 63            | TN = 215            |
Bu tabloya göre model, pozitif ve negatif sınıfları genel olarak dengeli şekilde ayırt edebilmiştir. Ancak pozitif sınıfa (iyi kalite şarap) ait bazı örnekleri kaçırdığı (FN), bazı negatifleri ise yanlış şekilde pozitif tahmin ettiği (FP) görülmektedir. Bu da modelin iyileştirilebilir yönleri olduğunu göstermektedir.
