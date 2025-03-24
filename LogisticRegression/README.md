Veri seti çeşitli özellikleri verilen helikopterlerlerin kaza yaptığı ve yapmadığı durumları göstermektedir. Kullanılan model de bu özelliklere göre helikopterin çarpıp çarpmayağını tahmin etmektedir.

Sınıflandırılmak istenilen veri setinde sınıf sayısı dengesiz olduğu için model helikopterlerin çarptığı durumları tahmin edememektedir bu yüzden azınlık sınıfını (Label = 1) çoğaltmak için Random Oversampling yöntemi kullanılmıştır. Böylece sınıf dağılımı dengelenmiş ve modelin her iki sınıfa da duyarlı olması sağlanmıştır.
Scikit-learn'de bulunan Logistic Regression modeli kullanılarak sınıflandırma yapılmıştır. Ayrıca, Ağırlıklı Gradient Descent algoritmasıyla sıfırdan Logistic Regression modeli yazılmıştır. Bu modelde sınıf dengesizliği için kayıplar ağırlıklandırılmıştır.

  | Özellik                | Scikit-learn Modeli        | Custom Logistic Regression |
  |------------------------|----------------------------|----------------------------|
  | Eğitim Süresi (saniye) | 0.09                       | 34.27                      |
  | Test Süresi (saniye)   | 0.0008                     | 0.0002                     |
  | Doğruluk (Accuracy)    | %55                        | %56                        |
  | Optimal Eşik Değeri    | -                          | 0.5179                     |
  
Sklearn modelinin training süresi custom modele göre çok daha kısa iken costom modelin test süresi minimal düzeyde daha hızlı gerçekleşmiş.
Custom model label = 0 durumlarını tahmin ederken daha iyi sonuç vermiş. Sklearn modelisi label = 1 durumlarında daha iyi performans göstermiş.
Ağırlıklandırma yaklaşımı ve eşik değerindeki farklar nedeniyle Scikit-learn modeli azınlık sınıfında daha yüksek Recall değerine ulaşırken, Özel Logistic Regression modeli her iki sınıfta daha dengeli bir performans göstermektedir.
KAYNAKÇA
https://www.kaggle.com/datasets/ehsanreghabi/helicopters-accidents-dataset
https://www.blog.trainindata.com/oversampling-techniques-for-imbalanced-data/
https://www.spiceworks.com/tech/artificial-intelligence/articles/what-is-logistic-regression/
