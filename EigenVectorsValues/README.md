Matris Manipülasyonu:
	Sayılarla oluşturulmuş iki boyutlu diziler olan matrisler üzerinde yapılan matematiksel işlemlerdir. Verinin temsil edilmesi, dönüştürülmesi ve analizi için temel bir araçtır. Veriler, özellikler ve parametreler makine öğrenmesinde genellikle matrisler olarak ifade edilir. Eğitim sürecinde yapılan hesaplamaların çoğu matris işlemleri ile gerçekleştirilir. Doğrusal regresyon, lojistik regresyon, sinir ağları, veri ön işleme, batch eğitim yöntemleri gibi birçok temel makine öğrenmesi yönteminde kullanılır.
Özdeğer (Eigenvalue):
	Bir kare matrise uygulandığında yalnızca ölçeklenen vektörlerin ne kadar ölçeklendiğini gösteren skalar değerlerdir. Veri içindeki varyansın hangi yönlerde yoğunlaştığını gösterir. Boyut indirgeme ve özellik çıkarımı gibi işlemlerde kullanılır. PCA, LDA, Spektral Kümeleme, Markov zincirleri, kontrol sistemleri gibi yöntemlerde kullanılır.
Özvektör (Eigenvector):
	Bir matris tarafından uygulanan dönüşümde yalnızca boyu değişen ama yönü değişmeyen vektörlerdir. Yani matrisin değiştirmediği doğrultuları temsil ederler. Verideki anlamlı yönleri temsil eder. Veriyi yeniden yönlendirme ve düşük boyutlu temsillere dönüştürme amacıyla kullanılır. PCA, SVD, Spektral Kümeleme, görüntü işleme (eigenfaces), graf temelli algoritmalar gibi yöntemlerde kullanılır.


numpy.linalg.eig, bir karesel matrisin özdeğerlerini ve özvektörlerini hesaplayan bir fonksiyondur. Özellikle lineer cebir ve makine öğrenmesi uygulamalarında yaygın olarak kullanılır. numpy.linalg modülü, NumPy'nin lineer cebir fonksiyonlarını içerir ancak eig fonksiyonu doğrudan Python'da yazılmamıştır. Bunun yerine LAPACK (Linear Algebra PACKage) adlı düşük seviyeli, yüksek performanslı bir kütüphaneyi kullanır.
Yüksek seviyeli Python arayüzü olarak çalışır. Arka planda, LAPACK içerisindeki dgeev veya zgeev gibi fonksiyonlara çağrı yapar. Bu LAPACK fonksiyonları C ve Fortran dillerinde yazılmıştır ve çok hızlıdır. Sonuç olarak, hem özdeğer hem de özvektörler çift olarak döndürülür.
linalg.py veya linalg/lapack_lite klasörü: Python ile LAPACK entegrasyonu burada yapılır. umath_linalg.c.src: Düşük seviyeli matematiksel işlemler burada tanımlıdır.
