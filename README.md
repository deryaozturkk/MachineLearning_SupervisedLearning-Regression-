# MachineLearning_SupervisedLearning-Regression
Makine Öğrenmesi Dersi Denetimli Öğrenme (Regresyon) Raporu
<p>
  <img width="700" height="350" src="https://user-images.githubusercontent.com/72493701/197514949-f969922b-0a4b-46f7-8916-22cebeb22c77.png">
</p>

###  İçindekiler:

+ Denetimli Öğrenme Nedir?
+ Tarihçesi
+ Denetimli öğrenme örnekleri
+ Regresyon Nedir Ve Çeşitleri Nelerdir?
+ Basit Doğrusal Regresyon Ve Çoklu Regresyon
+ Regresyon Analizi Nasıl Yapılır? Çalışma Mantığı Nedir?
+ Regresyon Analizi Kullanım Alanları
+ Regresyon Analizi Hangi Sektörlerde Var?
+ Denetimli Öğrenme Algoritmaları İle Basit Doğrusal ve Çoklu Regresyon Örnekleri
+ Kaynakça


# Denetimli Öğrenme
## Denetimli Öğrenme Nedir?
Denetimli öğrenme; aldığı veriler ve ürettiği sonuçlara dayalı olarak bir model geliştirme işlemidir. Diğer makine öğrenmesi türlerine kıyasla denetimli öğrenmenin en büyük farkı veri etiketi kullanılmasıdır. Etiketlediğimiz veriye, gösterdiğimiz sınıf ve bilgiye göre mevcut gerçekliğe dayanarak model geliştirme algoritmasıdır.
Örnekler üzerinde bir öğrenme sağlar ve yeni girdilerde de etiketi tahmin etmeye çalışır.
Denetimli öğrenmede, makine, bir öğrenme algoritması aracılığıyla etiketli eğitim verilerini çalıştırarak, gelir ve eğitim arasındaki ilişkiyi sıfırdan öğrenmeye çalışır. Denetimli öğrenmenin amacı, Y’nin bilindiği ve Y’nin bilinmediği yeni örnekler verildiğinde Y’yi mümkün olduğunca doğru bir şekilde tahmin etmektir. 
Örnek verecek olursak:
Spam ya da spam olmayan mailleri ayırt etmek için elimizde bir veri seti olsun. Bu veri setini kullanarak bir model eğitme işlemi denetimli öğrenmedir. 
### Tarihçesi
Denetimli öğrenme fikri Perceptron deneyi ile ortaya çıkmıştır. Bu deneyle yapay sinir ağının temelleri atılmıştır. 
1958 yılında psikolog Frank Rosenblatt tarafından üçgen ya da üçgen olmayan nesneleri belirlemek için bir çalışma yürütülüyor. Rosenblatt  zamanına göre yüksek kalitede kameralar(400 pixel) kullanarak oldukça büyük bir makine yapıyor ve buna da perceptron ismini veriyor. Perceptron tek katmanlı yapay sinir ağından oluşuyordu. 
Öğrenmeyi gerçekleştirmek için önce, kameraya çeşitli resimler gösteriyor. Deney için 2 sınıfımız var. Üçgen ya da değil.
Kamera gördüğü şeye bağlı olarak perceptrona farklı bir elektrik sinyal gönderiyor. Daha sonra Rosenblatt, üçgen şekliyle eşleşen tüm sinyalleri perceptrona uyguluyor. Eğer total skor threshold değerinden büyükse makine bir elektrik sinyali gönderir ve ışıklar açılır. Eğer elektriksel yük threshold değerinden küçükse ışık yanmıyor ve bu da üçgen olmadığı anlamına geliyor. İlk başta perceptron rastgele tahminler yaparak threshold değerini belirlemek için kullanıldı.Daha sonra Rosenblatt ‘evet’, ‘hayır’ butonlarıyla denetimli öğrenmeyi gerçekleştirdi. Eğer perceptron doğru tahmin yapıyorsa ‘evet’ tuşuna basıyordu,yanlış tahminde de sinapslardan geçen elektrik değerini ölçüp threshold değeri olarak belirliyordu.
Evet ,hayır butonları kullanıldığı için, bu uygulama denetimli öğrenmenin temeli sayıldı. 
### Denetimli öğrenme örnekleri:
Denetimli öğrenmenin ne olduğunu anlamak için bir örnek kullanacağız. Örneğin, bir çocuğa içinde on aslan, on maymun, on fil ve diğerleri gibi her türden on hayvanın bulunduğu 100 oyuncak hayvan veriyoruz. Daha sonra, çocuğa bir hayvanın farklı özelliklerine (özelliklerine) dayalı olarak farklı hayvan türlerini tanımayı öğretiyoruz. Rengi turuncuysa, o zaman bir aslan olabilir. Gövdesi büyük bir hayvansa, fil olabilir.Çocuğa hayvanları nasıl ayırt edeceğini öğretiriz, bu denetimli öğrenmeye bir örnektir. Şimdi çocuğa farklı hayvanlar verdiğimizde, onları uygun bir hayvan grubuna ayırabilmelidir.
<p>
  <img width="600" height="350" src="https://user-images.githubusercontent.com/72493701/197516059-c2af804a-bc65-4414-992e-5ca525b0242a.JPG">
</p>


Bunlara ek olarak en meşhur denetimli öğrenme uygulaması ,ev özelliklerine göre satış fiyatı tahmini yapmayı amaçlayan Boston konut fiyatı veri kümesidir. Ev özelliklerini kullanarak satış fiyatını tahmin etmeyi amaçlamıştır.
<p>
  <img width="600" height="350" src="https://user-images.githubusercontent.com/72493701/197578375-b63a1b22-918d-46f0-a353-696ed935b0e9.png">
</p>

## REGRESYON NEDİR?
Regresyon, bir bağımlı değişken (genellikle Y ile gösterilir) ve diğer bağımsız değişkenler arasındaki ilişkinin gücünü ve karakterini belirlemeye çalışan finans, yatırım, makine öğrenmesi ve diğer disiplinlerde kullanılan istatistiksel bir yöntemdir.

**Bağımlı Değişken:** Anlamaya veya tahmin etmeye çalıştığımız değişkendir. 

**Bağımsız Değişken:** Analizi veya hedef değişkeni etkileyen ve değişkenlerin hedef değişkenle ilişkisi hakkında bize bilgi veren faktörlerdir.

Makine öğrenmesinde regresyon ise kısaca makinenin veri setini ezberlememesi için oluşturulan algoritmadır. İstenen sonuç makinenin ezberlemesi değil “öğrenmesi” yani tutarlı tahmin yeteneğine sahip olmasıdır.
Yöntem olarak bir eğitim kümesi ve eğitim kümesinden makine öğrenmesi metotları ile bir model elde edilip bu model üzerinden yeni gelen veriler tahmin edilmeye çalışılır. Regresyon yönteminde tahmin sonucu kategorik değil nümerik bir değer olmalıdır. Örneğin: 

**Kategorik tahmin sonucu:** Hava çok soğuk, hava soğuk, hava ılık, hava sıcak, hava çok sıcak gibi.

**Nümerik tahmin sonucu:** Hava -10 derece, 0 derece, 10.01 derece, 30.02 derece gibi sayısal değerlerdir.
<p>
  <img width="400" height="250" src="https://user-images.githubusercontent.com/72493701/197579105-95db7c93-abf2-4531-9f95-2ed39c15bdc9.png">
</p>

**1-Doğrusal Regresyon:** Doğrusal regresyon, iki değişken arasındaki doğrusal ilişkinin bir doğru denklemi olarak tanımlanıp, değişkenin değerlerinden biri bilindiğinde diğeri hakkında tahmin yapılmasını sağlar.
İş arkadaşlarınızın daha önce zaten anladıklarını görmüş ve düşünmüş olabilecekleri kalıpları ve ilişkileri ortaya çıkararak daha iyi iç görüler sağlamak için de doğrusal regresyondan yararlanabilirsiniz. Örneğin, satış ve satın alma verilerini analiz etmek, belirli günlerdeki ya da belirli saatlerdeki belirli satın alma kalıplarını ortaya çıkarmanıza yardımcı olabilir. Regresyon analizinden toplanan iç görüler, iş liderlerinin şirketlerinin ürünlerinin yüksek talep göreceği zamanları tahmin etmelerine yardımcı olabilir.
Doğrusal regresyon, basit doğrusal regresyon ve çoklu doğrusal regresyon olarak iki başlık altında incelenir.
**Basit doğrusal regresyon**, yanıt değişkeni ile tek bir açıklayıcı değişken arasındaki doğrusal ilişkiyi açıklar. Eğer tek bir yanıt değişkeni ve birden fazla açıklayıcı değişken arasındaki doğrusal veya eğrisel bir ilişki tanımlanmak istenirse, ilişki **çoklu doğrusal regresyon** ile incelenir (Okur, 2009; Weisberg, 2005).

**2-Polinom Regresyon:** Bir bağımlı ve birden fazla bağımsız değişken arasında polinomal bir artış söz konusu ise bu algoritmayı kullanırız. Polinom Regresyon Formülü: Y = a + bX + cX²

**3-Karar Ağacı Regresyonu:** Karar Ağaçları Algoritmaları hem sınıflandırma da hem de regresyonda kullanılır. Regresyon için kullanılan algoritmayı şöyle açıklayabiliriz; Bağımsız değişkenleri bilgi kazancına göre aralıklara ayırır. Tahmin esnasında bu aralıktan bir değer sorulduğunda cevap olarak bu aralıktaki (eğitim esnasında öğrendiği) ortalamayı verir. Belli aralıklarda istenilen değerler için aynı sonuçları ürettiğinden kesikli bir modeldir.

**4-Lojistik Regresyon:** Lojistik regresyon, istatistikte kullanılan bir model oluşturma tekniği olup iki ya da daha fazla sınıfta ifade edilebilen kesikli verilerde yanıt değişkeni (Y) için bir model oluşturma tekniğidir.
Örneğin, web sitesi ziyaretçinizin alışveriş sepetindeki ödeme düğmesine tıklayıp tıklamayacağını tahmin etmek istediğinizi varsayalım. Lojistik regresyon analizi, web sitesinde harcanan zaman ve sepetteki ürün sayısı gibi geçmiş ziyaretçi davranışlarına bakar. Geçmişte, ziyaretçiler sitede beş dakikadan fazla zaman geçirdiyse ve sepete üçten fazla ürün eklediyse ödeme düğmesine tıkladıklarını belirler. Lojistik regresyon işlevi bu bilgiyi kullanarak daha sonra yeni bir web sitesi ziyaretçisinin davranışını tahmin edebilir.

**5-Ridge Regresyon:** Lasso Regresyon, Sıralı Regresyon gibi daha birçok regresyon türü bulunmaktadır.
<p>
  <img width="400" height="250" src="https://user-images.githubusercontent.com/72493701/197581630-2c4a20bd-4108-44b0-913e-7f6659142c89.png">
</p>

### Basit Doğrusal Regresyon
Açıklayan(bağımlı) ile  tek bir açıklayıcı (bağımsız) değişkenin arasındaki doğrusal ilişkinin modellenmesidir. Bir başka ifadeyle bağımlı değişkenin değerini bağımsız denklemin bir fonksiyonu olarak en doğru şekilde tahmin eden doğrusal ilişkidir. Burada tahmin edilmek istenen bağımlı değişkendir.
İki değişken arasındaki ilişkinin ne kadar güçlü olduğu
Bağımsız değişkenin belirli bir değerinde bağımlı değişkenin değeri
Bilgilerine ulaşmak için basit doğrusal regresyon kullanılır.
Gelir ve mutluluk arasındaki ilişkiyle ilgilenen bir araştırmacı olduğunuzu düşünün. Gelirleri 15 bin ile 75 bin arasında değişen 500 kişiyi araştırıyorsunuz ve onlardan mutluluklarını 1'den 10'a kadar puanlamalarını istiyorsunuz.
Bağımsız değişkeniniz (gelir) ve bağımlı değişkeniniz (mutluluk) niceldir, bu nedenle aralarındaki ilişkiyi basit doğrusal regresyon analizi ile açıklayabilirsiniz.

### Basit Doğrusal Regresyon Hesaplamaları
<p>
  <img width="150" height="50" src="https://user-images.githubusercontent.com/72493701/197583620-647fe0df-c0c0-42b2-b7ba-b30fea6bb03f.png">
</p>

+ y= yanıt değişkeni
+ B0 = kesim noktası
+ B1 = doğrunun eğimi
+ x=bağımsız değişken
+ e=hata payı(kalıntı)

#### E Nedir?
Gerçek değer ve tahmini değer arasındaki farktır.
Bu farka göre modeller arasındaki doğruluk kontrolü yapılır.
<p>
  <img width="150" height="50" src="https://user-images.githubusercontent.com/72493701/197585822-f4b76e3e-1d60-4ca0-8928-a9e336bc6427.png">
</p>

- yi = gerçek değer
- ŷi  = tahmini çıktı
- 
Bir pazarlama firmasının televizyon, gazete ve radyoya verdiği reklamların satışlar üzerindeki etkisini araştırdığını varsayalım.

           satışlar ≈β0+β1×TV
           
satışlar ve TV değişkenleri   arasındaki doğrusal model formülize edildiği gibidir.

Satışlar ve TV değişeninin regresyon fonksiyonu;
<p>
  <img width="150" height="50" src="https://user-images.githubusercontent.com/72493701/197586440-695342e6-cb03-40fe-8bd8-64bdac07389f.png">
</p>
şeklinde ifade edilir.
<p>
  <img width="600" height="300" src="https://user-images.githubusercontent.com/72493701/197587586-0106789d-f080-44ca-9a5f-4664d1bf9c17.png">
</p>

Basit doğrusal regresyon analizi sonucu parametre kestirimlerinin güvenli olabilmesi için bazı varsayımların geçerli olması gereklidir .
Modeldeki bağımsız değişkenlerin, bağımlı değişkeni ne kadar açıkladığı R2 değeri ile ölçülür.

R2 değerini hesaplamak için 
- Toplam Kareler Toplamı
- Artık Kareler Toplamı
değerlerine ihtiyaç duyarız.
<p>
  <img width="800" height="350" src="https://user-images.githubusercontent.com/72493701/197588048-0b0b0a68-cf19-42af-85a1-37a323038267.png">
</p>

R2  0-1 arasında bir değer alır. R2 değerinin 1’e yakın olması bağımsız değişkenlerin, bağımlı değişkenleri iyi bir şekilde açıkladığını gösterir.
<p>
  <img width="400" height="100" src="https://user-images.githubusercontent.com/72493701/197588577-47b00fbf-4cee-43e0-a3d7-4fa2ede1ca50.png">
</p>

### Çoklu Regresyon
Doğrusal regresyon bir bağımsız değişkenin bir bağımlı değişken üzerine etkisini göstermeye yararken, çoklu regresyonda bağımsız değişken sayısı birin üstüne çıkar. 
En az iki bağımsız değişkenin, bağımlı değişken üzerinde etkilerini göstermeye yarayan analiz yöntemidir.
İki değişken varsa, tahminin temelini oluşturan değişken bağımsız değişkendir. Değeri tahmin edilecek değişken bağımlı değişken olarak bilinir.

      Y=a0+a1X1+a2X2+...+akXk+ei =a0+ΣarXr+e 

      y = ß0 + ß1.x1 + ß2.x2 + ... + ßk.xk+ei = ß0+ΣßrXr+e
Çoklu lineer regresyonda her bağımsız değişkenin bağımlı değişkene etkime derecesi birbirinden farklıdır. Bundan dolayı basit lineer regresyondaki denkleme ek olarak her değişkenin katsayısı aynı olmak zorunda değildir. 

#### P Değeri Nedir?
**P değeri, bizim hipotezlerimizin doğru olup olmadığını belirlememize yardımcı olan istatistiksel bir ölçüdür.**
P değerleri, deney sonuçlarının gözlemlenen olaylar için normal değerler aralığında olup olmadığını belirlemek için kullanılır. 
Genellikle, bir veri setinin P değeri önceden belirlenmiş belirli bir miktarın altındaysa (örneğin, 0.05 gibi), bilim insanları deneylerinin "boş hipotezini" reddedeceklerdir.
Yani ilgili değişkenin sonuç üzerinde anlamlı bir etkisinin olmadığı anlaşılır.

#### Çoklu Lineer Regresyon Modeli Oluşturmak
Çoklu lineer regresyon modeli oluştururken oldukça fazla parametrenin dikkatle incelenmesi gerekir, çünkü her bir değerin bağımlı değişken üzerinde anlamlı bir etkisi olmayabilir. 
Bağımlı değişkeni yüksek oranda etkileyen bir değişkeni veri setinden kaldırdığımız zaman oluşacak hatalar veya gereksiz bir değişkeni veri setinden atmadığımız zaman kaybedeceğimiz verim istenilmeyen bir sonuçtur.
Bu durumu doğru şekilde incelemek için belirli istatistik modelleri vardır. 
#### Regresyon Modeli Kurulumunda 5 Metod

1. Bağımsız değişkenlerin hepsini birden modele dahil etmek (All-in)
2. Geriye doğru eleme (Backward Elimination)
3. İleriye doğru seçme (Forward Selection):
4. İki yönlü eleyerek seçme (Bidirectional Elimination)
5. Sonuçları karşılaştırma (Score comparision)

##### Geriye Doğru Eleme
Geriye doğru eleme yöntemi tüm değişkenleri içeren bir modelden, fazlalıklarını atarak daha verimli daha küçük bir model oluşturma içeren algoritmadır.
1. Değişkenlerin modelde kalması için önem değeri belirlenir. Bir çeşit eşik değeri(threshold) olarak işlev görür. (p<0.05) 
2. Modelle alakasız değişkenler modelden çıkarılır.
3. En yüksek P değerine sahip değişkeni bul. Eğer önem değerinden yüksekse (P>SL) bir sonraki adıma ilerle. Eğer düşükse modelin geriye doğru eleme algoritmasını tamamlamıştır.
4. P değeri önem değerinden yüksek değişkeni modelden çıkart ve 3. adıma dön.

##### İleri Doğru Seçme

İleri doğru seçme yöntemi geriye doğru eliminasyon yönteminden farklı olarak hiçbir bağımsız değişken içermeyen bir model olarak başlar yolculuğuna. Sonrasında ise hipoteze en yararlı olduğu tahmin edilen değişkenleri alarak kendisini daha büyük bir model haline getirir. İşleyişi ise şöyledir:
1. Modele giriş için bir önem değeri belirlenir. (Örneğin SL=0,05)
2. Bütün bağımsız değişkenler ve bağımlı değişkenle ayrı ayrı ikişerli modeller oluşturulur. En küçük P değerine sahip değişken seçilir.
3. Seçilen değişken modele eklenir. Bundan sonrasında ise belirlenen önem değerinden düşük olmakla beraber yine en küçük P değerine sahip değişken modele eklenir.
4. Bu işlem seçilen yeni değişkenin P değerinin önem değerinden fazla olmasına kadar devam eder. En küçük P değerine sahip yeni değişkenin P değerinin önem değerinden fazla olduğunu gördüğümüzde daha önce eklediğimiz değişkenlerin model için yeterli olduğunu anlamalıyız.
5. Bu yazıda sizleri daha fazla yöntemle karmaşaya boğmak istemiyorum. Çok yönlü eleme yöntemi hakkında bilgi sahibi olmak isterseniz "bidirectional elimination" anahtar kelimesiyle araştırma yapabilirsiniz.

### Regresyon Analizi Nasıl Yapılır? Çalışma Mantığı Nedir?
Bir regresyon analizi 3 adımda gerçekleştirilir. 
1. Öncelikle bir hipotez oluşturulur
Bir regresyon analizi yapmak için, ilişkili olduğuna inandığınız iki değişkeni seçmeniz gerekir. Mümkün olduğu kadar çok veri toplayarak ilişkileri hakkında hipotezinizi oluşturun. Reklam ve satış ilişkisi söz konusu olduğunda, daha doğru bir analiz için bir yıl boyunca oluşan tüm finansal verileri toplayabilirsiniz.
2.  Bir grafik oluşturulur
Bir sonraki adım, verilerinizin grafiğini çıkarmaktır. İki veri seti ile doğrusal regresyon için temel bir çizgi grafiği oluşturabilirsiniz. Bir değişken X ekseninde, diğeri Y ekseninde çizilir. Bir elektronik tabloya girdiğinizde, değişkenler arasındaki korelasyonu görebilirsiniz. Düz bir çizgi varsa, bu pozitif bir korelasyon gösterir.
<p>
  <img width="400" height="250" src="https://user-images.githubusercontent.com/72493701/197591897-23263809-773b-426e-94fc-15105231fd25.png">
</p>
3. Sonuçlar analiz edilir
Grafiği temel bir doğrusal regresyonda inceleyerek kesişim, katsayı ve korelasyonu görebilirsiniz. Bu rakamları bir araya getirmek, iki veri seti arasındaki tarihsel ilişkiyi göstererek modelin gelecekte nasıl görüneceğini tahmin etmenize olanak tanır. Geçmişte, çevrimiçi reklamcılık ve satışlar arasında olumlu bir ilişki varsa, gelecek yıl için bir tahmin oluşturmak için yüzdeleri bir modele ekleyebilirsiniz. 
<p>
  <img width="500" height="300" src="https://user-images.githubusercontent.com/72493701/197591700-c842cf6e-5bb3-4b89-b2db-9ce4620edbb8.png">
</p>

### Regresyon Analizi Kullanım Alanları

1. Tahmin

İşletmelerde regresyon analizinin en yaygın kullanımı, **gelecekteki fırsatları ve tehditleri tahmin etmektir**. Örneğin talep analizi, bir müşterinin satın alma olasılığı yüksek olan şeylerin miktarını tahmin eder.
Ancak iş söz konusu olduğunda, talep tek bağımlı değişken değildir. **Regresif analiz**, doğrudan gelirden çok daha fazlasını öngörebilir.
Örneğin, belirli bir reklam panosunun önünden geçecek tüketicilerin sayısını tahmin ederek bir reklam için en yüksek teklifi tahmin edebilir.

2. CAPM

Bir varlığın öngörülen getirisi ile ilgili piyasa risk primi arasındaki bağlantıyı kuran **The Capital Asset Pricing Model (CAPM), doğrusal regresyon modeline dayanır.** Ayrıca, kurumsal getirileri ve operasyonel performansı tahmin etmek için finansal analistler tarafından finansal analizde sıklıkla kullanılır.
Bir hisse senedinin beta katsayısı, regresyon analizi kullanılarak hesaplanır. Beta, toplam piyasa riskiyle ilgili getiri oynaklığının bir ölçüsüdür.

3. Rekabet karşılaştırma 

Bir şirketin finansal performansını belirli bir muadili ile karşılaştırmak için kullanılabilir. Ayrıca iki firmanın hisse senedi fiyatları arasındaki ilişkiyi belirlemek için de kullanılabilir ve hangi yönlerin satışlarını etkilediğini belirlemede firmaya yardımcı olabilir. Bu teknikler, küçük işletmelerin kısa sürede hızlı başarıya ulaşmalarına yardımcı olabilir.

4. Güvenilir kaynak

Birçok işletme ve üst düzey yönetici, daha iyi iş kararları vermek, varsayımları ve içgüdüleri azaltmak için regresyon analizini kullanır. Yöneticiler, verileri filtrelemek ve mümkün olan en iyi kararları vermek için regresyon analizinden yararlanır.

### Regresyon Analizi Hangi Sektörlerde Var?  
Regresyon analizinin nerelerde kullanılabileceğini öğrenmek istiyorsanız, aşağıdaki örnekleri inceleyebilirsiniz.

**Finans Sektörü:**

Finansta, bir hisse senedinin BETA’sını hesaplamak için regresyon analizi kullanılır. Üstelik bunu Excel yardımı ile kolayca yapabilirsiniz.
Yine finansta, şirketler için mali tabloları tahmin etmek için regresyon analizi de kullanılır. Böylece, iş varsayımlarındaki hangi değişikliklerin gelecekteki giderleri ve geliri etkileyeceğini belirleyebilirsiniz.
Bir şirketin satışları son birkaç yıldır her ay istikrarlı bir şekilde arttıysa, satış verileri üzerinde aylık satışlarla doğrusal bir analiz yaparak şirketin gelecek aylardaki satışlarını tahmin edebilirsiniz.
Bir firmanın yöneticisi, gelecek planlaması için reklam harcamaları ile satışlar arasındaki kesin ilişkiyi öğrenmek istiyorsa, regresyon tekniği ile bu ilişkiyi tahmin edebilir.

**Pazarlama:**

 Pazar kampanyalarının etkinliğini, tahmin fiyatlandırmasını ve ürünün satışını anlamak.
 
**Üretim:**

 Daha iyi performans sağlamak için değişkenlerin ilişkisini değerlendirmek.
 
**İlaç:**

 Hastalıklar için jenerik ilaçlar hazırlamak için farklı ilaç kombinasyonlarını tahmin etmek.

### Denetimli Öğrenme Algoritmaları İle Basit Doğrusal ve Çoklu Regresyon Örnekleri

1. İşletmeler, reklam harcamaları ile gelir arasındaki ilişkiyi anlamak için genellikle doğrusal regresyon kullanır.
  <p><img width="200" height="50" src="https://user-images.githubusercontent.com/72493701/197595507-4485719b-f0d0-4a69-b946-0aa74927cff5.png">
</p>
+ Β0 katsayısı, reklam harcaması sıfır olduğunda beklenen toplam geliri temsil eder.
+ Β1 katsayısı, reklam harcamaları bir birim (ör. Bir dolar) artırıldığında toplam gelirdeki ortalama değişimi temsil eder.
+ Β1 negatifse, bu, daha fazla reklam harcamasının daha az gelirle ilişkili olduğu anlamına gelir.
+ Β1 sıfıra yakınsa, bu, reklam harcamalarının gelir üzerinde çok az etkisi olduğu anlamına gelir.
+ Β1 pozitifse, daha fazla reklam harcamasının daha fazla gelirle ilişkili olduğu anlamına gelir.
+ Β1 değerine bağlı olarak, bir şirket reklam harcamalarını azaltmaya veya artırmaya karar verebilir.

2. Tıbbi araştırmacılar, ilaç dozu ile hastaların kan basıncı arasındaki ilişkiyi anlamak için sıklıkla doğrusal regresyon kullanırlar.

Örneğin, araştırmacılar hastalara belirli bir ilacın çeşitli dozajlarını uygulayabilir ve kan basıncının nasıl tepki verdiğini gözlemleyebilir. Yordayıcı değişken olarak dozajı ve yanıt değişkeni olarak kan basıncını kullanan basit bir doğrusal regresyon modeline uyabilirler. Regresyon modeli aşağıdaki formu alacaktır:
<p>
  <img width="200" height="50" src="https://user-images.githubusercontent.com/72493701/197597269-71c8ea85-85ce-4ef0-bc20-45d8ae78fece.png">
</p>

+ Β0 katsayısı, dozaj sıfır olduğunda beklenen kan basıncını temsil eder.
+ Β1 katsayısı, dozaj bir birim artırıldığında kan basıncındaki ortalama değişimi temsil eder.
+ Β1 negatif ise, dozajdaki bir artışın kan basıncındaki bir düşüşle ilişkili olduğu anlamına gelir.
+ Β1 sıfıra yakınsa, bu, dozajdaki bir artışın kan basıncında herhangi bir değişiklik olmaması ile ilişkili olduğu anlamına gelir.
+ Β1 pozitif ise, dozajdaki bir artışın kan basıncındaki bir artışla ilişkili olduğu anlamına gelir.
+ Β1 değerine bağlı olarak, araştırmacılar bir hastaya verilen dozu değiştirmeye karar verebilir.

3. Tarım bilimcileri, gübre ve suyun mahsul verimi üzerindeki etkisini ölçmek için genellikle doğrusal regresyon kullanırlar.

Örneğin, bilim adamları farklı alanlarda farklı miktarlarda gübre ve su kullanabilir ve bunun mahsul verimini nasıl etkilediğini görebilirler. Yordayıcı değişkenler olarak gübre ve su ve yanıt değişkeni olarak mahsul verimi kullanan çoklu doğrusal regresyon modeline uyabilirler. Regresyon modeli aşağıdaki formu alacaktır:
<p>
  <img width="400" height="50" src="https://user-images.githubusercontent.com/72493701/197597888-edbc2b23-13c1-436b-936d-d021a5a1f1b1.png">
</p>

+ Β0 katsayısı, gübre veya su olmadan beklenen mahsul verimini temsil eder.
+ Β1 katsayısı, su miktarının değişmeden kaldığı varsayılarak, gübre bir birim artırıldığında mahsul verimindeki ortalama değişimi temsil edecektir.
+ Β2 katsayısı, gübre miktarının değişmeden kaldığı varsayılarak, su bir birim artırıldığında mahsul verimindeki ortalama değişimi temsil edecektir.
+ Β1 ve β2 değerlerine bağlı olarak, bilim adamları mahsul verimini en üst düzeye çıkarmak için kullanılan gübre ve su miktarını değiştirebilirler.

4. Gayrimenkul örneği

Ev satmak için en iyi zamanı tahmin etmeye yardımcı olacak bir model oluşturmak isteyen bir emlak uzmanısınız. Evleri maksimum satış fiyatından satmak istersiniz, ancak satış fiyatını birden fazla faktör etkileyebilir. Bu değişkenler, diğer faktörlerin yanı sıra evin yaşını, mahalledeki diğer evlerin değerini, devlet okulu sisteminin öğrenci performansına ilişkin nicel ölçümlerini ve yakındaki parkların sayısını içerir.Evlerin maksimum satış fiyatını tahmin etmek için bu dört bağımsız değişkenden bir tahmin modeli oluşturabilirsiniz. Bu faktörlerden herhangi biri katsayı değerleri açısından değişirse değişkenleri ayarlayabilirsiniz.

5. İş örneği

Halka açık bir şirkette hisse senediniz var ve şimdi hisse senedinizi satmak için iyi bir zaman olup olmayacağını bilmek istiyorsunuz. Şirketin karlılığı, şirketin maliyetleri, şirketin rekabeti ve şirketin varlıkları dahil olmak üzere hisse senedi fiyatının değerini çeşitli değişkenler etkileyebilir. Hisse senedini hemen satmanız mı yoksa hisse senedini elinde tutmaya devam etmeniz mi gerektiğine karar vermenize yardımcı olmak için bu dört bağımsız değişkenden bir tahmin modeli oluşturabilirsiniz
 6. Halk sağlığı örneği
 Bulaşıcı bir hastalığın yayılmasını inceleyen bir epidemiyologsunuz. Mevcut bilinen enfeksiyonlara dayanarak bu hastalığın gelecekteki yayılmasını tahmin etmek istiyorsunuz. Çok sayıda bağımsız değişken, popülasyon büyüklüğü, popülasyon yoğunluğu, hava sıcaklığı, asemptomatik taşıyıcılar ve popülasyonun sürü bağışıklığına ulaşıp ulaşmadığı dahil olmak üzere gelecekteki enfeksiyonların sayısını etkileyebilir. Yordayıcı değişkenlerin katsayı değerlerindeki olası değişiklikleri hesaba katan bir sonucu tahmin etmek için ampirik veriler üzerinde istatistiksel modelleme ve çoklu doğrusal regresyon analizi yapabilirsiniz.


 #### KAYNAKÇA

+ https://en.wikipedia.org/wiki/Simple_linear_regression
+ https://dergipark.org.tr/en/download/article-file/187511
+ https://aws.amazon.com/tr/what-is/logistic-regression/
+ https://www.ibm.com/tr-tr/analytics/learn/linear-regression
+ https://www.scribbr.com/statistics/simple-linear-regression/#:~:text=What%20is%20simple%20linear%20regressio%20n,Both%20variables%20should%20be%20quantitative.
+ https://www.youtube.com/watch?v=4qVRBYAdLAo
+ https://www.cancankiran.com/makine-ogrenimi/
+ https://www.statology.org/linear-regression-real-life-examples/














