Bu çalışmanın amacı, bir mobil telefon fiyat tahmin modelini Gaussian Naive Bayes algoritması ile eğiterek, sklearn kütüphanesi ile manuel olarak yazılan bir Naive Bayes sınıflandırıcısının performanslarını karşılaştırmaktır. Model, telefon özelliklerine göre fiyat aralığını tahmin etmek üzerine kurulmuştur.
Kullanılan veri seti, telefonlara ait çeşitli teknik özellikleri ve fiyat aralığı bilgilerini içermektedir. Modelde "battery_power", "int_memory", "ram", "clock_speed", "dual_sim" ve "price_range" değişkenleri kullanılmıştır.
"price_range" değilkeni ikili sınıflandırmaya uygun olacak şekilde düzenlenmiştir.
Öncelikle veri setine preprocessing yapılmıştır, ardından Sklearn GaussianNB kullanılarak Naive Bayes sınıflandıran model eğitilmiştir. Veri setindeki değişkenler sürekli olduğundan dolayı Gauissian Naive Bayes tercih edilmiştir. Daha sonra aynı işlemler sklearn kütaphenesi kullanmadan python sınıfı olarak oluşturulan bir modelle tekrarlanmıştır. Son olarak modellerin çalışma süreleri ve confusion matrixleri incelenmiştir.
Manuel model, Sklearn modeline kıyasla daha hızlı eğitilmiştir. Sklearn modelinin ise test süresi daha kısa sürmüştür. Modellerin confusion matrix sonuçları aynı çıkmıştır.
False negative değerlerin false pozitive değerlerden fazla olması nedeniyle recall değeri precisiona göre daha fazla önem arz etmektedir. Confusion matrixin sonuçları görece yüksektir.

KAYNAKÇA
https://www.kaggle.com/datasets/jacksondivakarr/phone-classification-dataset/data
https://scikit-learn.org/stable/modules/naive_bayes.html
https://www.geeksforgeeks.org/gaussian-naive-bayes/
https://medium.com/@gulcanogundur/do%C4%9Fruluk-accuracy-kesinlik-precision-duyarl%C4%B1l%C4%B1k-recall-ya-da-f1-score-300c925feb38

