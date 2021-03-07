# Google DSC - Solution Challange Hack for People Hackathon | trAI

Google DSC tarafından düzenlenen Solution Challenge Hack for People & Peace Hackathon'u için oluşturulan trAI projesi. Bu repoda trAI'ın Yapay Zeka (AI) ve Bilgisayarlı Görü (CV) teknolojileri işlenmiştir. Mobil uygulama çözümleri için buradaki repoyu inceleyebilirsiniz.

Amacımız, Google teknolojilerini kullanarak geliştirdiğimiz trAI çözümleri ile Birleşmiş Milletilerin yayınladığı [*Sürdürülebilir Kalkınma Amaçları*](https://www.tr.undp.org/content/turkey/tr/home/sustainable-development-goals.html)'na katkı sağlamaktır. Bu proje, Sağlık ve Kaliteli Yaşam (Hedef 3) başlığı altında yer alan Bulaşıcı Olmayan Hastalıklardan Kaynaklanan Ölümlerin Azaltılması ve Ruh Sağlığının Desteklenmesi (Hedef 3.4) konusu ile ilgilidir.

<p align="center">
  <img width="600" src="https://github.com/oreitor/google-hack-for-people-hackathon/blob/main/trAI.png">
</p>

trAI için Hackathon'un bu aşamasında belirlenen ana hedef, AI, CV ve Mobil Uygulama çözümleri ile kullanıcının yiyecek ve egzersiz takibini yaparak bireyin yaşam kalitesini fiziksel ve mental açıdan arttırmaktır. 

Yiyecek (Food) ve egzersiz (Training) olarak iki farklı başlık olarak ele aldığımız trAI'ın genel hatlarıyla belirttiğimiz AI ve CV mimarisi ve bu süreçte kullandığımız Google teknolojileri aşağıda ifade edilmiştir. 

#### 5 Farklı AI ve CV Karar Mekanizması
* Yiyecek tanımlama ve algılama
* Yiyecek besin değerleri ve kullanıcı alışkanlıkları arasındaki ilişkiyi ele alacak Derin Öğrenme yapısı
* İnsan vücudu ile egzersiz tanımlama ve algılama
* Egzersiz özellikleri ve kullanıcı alışkanlıkları arasındaki ilişkiyi ele alacak Derin Öğrenme yapısı
* Yiyecek ve Egzersiz arasındaki korelasyonu ve çıktıları oluşturacak Makine Öğrenmesi yapısı

#### AI ve CV için Kullanılan Google Teknolojileri
* Tensorflow
* Google Cloud Platform
* Google Cloud Vision API

## trAI - Food
Projemizin yiyecek tarafında Google Cloud Vision API tarafından sunulan çözümler tercih edilmiştir. Böylelikle yiyecekleri sınıflandırma süreci Google altyapsı sayesinde hem daha efektif hale gelmiş hem de günümüz teknolojileri son haliyle kullanılmıştır. Şu anki süreçte oluşturduğumuz [Food Recognition](https://github.com/oreitor/google-hack-for-people-hackathon/blob/main/Food%20Recognition/food_recognition.ipynb) algoritmamız 6 farklı kategoride 40 farklı yiyecek sınıfını yüksek doğruluk değerleri ile tespit edebilmektedir. İlgili yiyecek sınıfları için Google görsellerden rastgele seçilmiş görüntülerle oluşturduğumuz veri havuzuna [buradan](https://github.com/oreitor/google-hack-for-people-hackathon/tree/main/Food%20Recognition/images) ulaşabilirsiniz.

Bununla birlikte sınıflandırılan yiyecekler [Nutritional values for common foods and products](https://www.kaggle.com/trolukovich/nutritional-values-for-common-foods-and-products) kaynağından alınan besin değeri bilgileri içeren [veriseti](https://github.com/oreitor/google-hack-for-people-hackathon/blob/main/Food%20Recognition/nutrition.csv) ile ilişkilendirilmiştir. Bu veriseti 8789 farklı yiyecek kombinasyonunu 77 farklı besin değeri ile her bir durum için 100 gram üzerinden ifade etmektedir. Algoritmamızda şu an için 77 farklı besin değeri içerisinden *Kalori, Yağ, Şeker ve Protein* olmak üzere popüler olan 4 farklı besin değeri ele alınmıştır.

Yiyecek sınıflandırması yapıldıktan sonra ilgili besin değerleri verisetinden çekilerek test görüntüsü üzerinde aşağıdaki görsellerde olduğu gibi belirtilmektedir. 

<p align="center">
  <img width="300" src="https://github.com/oreitor/google-hack-for-people-hackathon/blob/main/Food%20Recognition/test_images/pizza.jpg"><span> &emsp;</span>
  <img width="250" src="https://github.com/oreitor/google-hack-for-people-hackathon/blob/main/Food%20Recognition/test_images/pomegranate.jpg"><span> &emsp;</span>
  <img width="200" src="https://github.com/oreitor/google-hack-for-people-hackathon/blob/main/Food%20Recognition/test_images/potato,.jpg">
</p>

<p align="center">
  <img width="250" src="https://github.com/oreitor/google-hack-for-people-hackathon/blob/main/Food%20Recognition/test_images/orange.jpg"><span> &emsp;</span>
  <img width="200" src="https://github.com/oreitor/google-hack-for-people-hackathon/blob/main/Food%20Recognition/test_images/cookie.jpg"><span> &emsp;</span>
  <img width="200" src="https://github.com/oreitor/google-hack-for-people-hackathon/blob/main/Food%20Recognition/test_images/egg.jpg">
</p>

Bahsedilen yapı sadece şu anki geldiğimiz aşamayı ifade etmekle birlikte yapılacak geliştirmelerle binlerce farklı sınıf eklenebilir. Bununla birlikte yiyecek algılama esnasında çekilen görüntüdeki yiyeceğin hacimsel özellikleri de ilerleyen aşamalarda farklı metadolojiler kullanılarak belirlenebilmektedir.
