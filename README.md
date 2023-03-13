# GAIH_Akabank_Python_Bootcamp Pizza Order Automation (Turkish):


Project Overview

Pizzacı Dükkanı mı açmak istiyorsunuz? O zaman bu proje hayalinizdeki proje olabilir. Proje,
kullanıcıların kendi pizzalarını tasarlamalarını ve ödeme yaptıktan sonra kullanıcıyı veri
tabanına eklemelerini hedefliyor. Peki bu projede ne tür görevlerimiz var?
Pizza Sipariş Sistemi, kullanıcıların menüdeki pizzayı ve istedikleri sosları seçmesiyle başlar.
Seçtikleri sos ve pizzayı seçtikten sonra ödemek zorundalar. Kullanıcılar ödemelerini kredi
kartı ile yapacaktır. Her pizzanın bir açıklaması ve fiyatı vardır. Bu değerlerin sınıflar içinde
sabit bir değer olarak ayarlanması gerektiğine dikkat edin.

1. Google Colab Dosyası Oluşturma
● Projenizin .ipynb veya .py uzantısına sahip olduğundan emin olun.
● Projenizde ayrıntıları açıklayan yorum satırları olduğundan emin olun.

2. Gerekli Kitaplıkları İçe Aktarma
● Import csv
● Import datetime

3. “Menu.txt” dosyasını oluştur
● Menu.txt adlı bir dosya oluşturun ve içine aşağıdaki metni yazın.
* Lütfen Bir Pizza Tabanı Seçiniz:
1: Klasik
2: Margarita
3: TürkPizza
4: Sade Pizza
* ve seçeceğiniz sos:
11: Zeytin
12: Mantarlar
13: Keçi Peyniri
14: Et
15: Soğan
16: Mısır
* Teşekkür ederiz!

4. Üst sınıf oluştur “pizza”
● Pizza sınıfını ve bu sınıfın içindeki encapsulation(kapsülleme) için get_description()
ve get_cost() yöntemlerini tanımlayın.
○ Bu açıklama hazırlanan pizzanın kısa bir açıklaması olmalıdır!

5. Alt sınıf oluştur “pizza”
● Klasik, Margherita, Türk Pizzası, Dominos Pizza vb. pizza sınıfları oluşturun. Bu
pizza türlerinin her biri bir pizza türü olduğu için bu sınıflar alt sınıflar olarak
tanımlanacaktır.
○ Her pizzanın kendine ait bir fiyatı ve sahip olduğu değişkenin içinde pizzaların
açıklamasının yer alması gerektiğini unutmayın.

6. Üst sınıf oluştur “Decorator”
● Bir Decorator sınıfı oluşturun. Decorator, burada tüm sos sınıflarının süper sınıfı
olarak adlandırılır.
● Decorator sınıfı, pizza sınıfının özelliklerini kullanarak get_description() ve get_cost()
yöntemlerini kullanacaktır. Aşağıdaki yöntemleri kullanarak decorator sınıfını
tamamlayın.
def get_cost(self):
return self.component.get_cost() + \
Pizza.get_cost(self)
def get_description(self):
return self.component.get_description() + \
' ' + Pizza.get_description(self)
● Sos olarak Zeytin, Mantar, Keçi Peyniri, Et, Soğan ve Mısır'ı belirleyin ve belirlediğiniz
sosların her birini bir sınıf olarak tanımlayın.
○ Unutmayın ki her sosun kendine ait bir fiyatı ve değişken olarak her bir
pizzanın açıklaması olması gerekir.
● Bir main fonksiyonu oluşturun. Bu fonksiyon önce menüyü ekrana yazdıracaktır.
Ardından kullanıcının menüden bir pizza ve sos seçmesine imkan tanıyacaktır.
Seçilen ürünlerin toplam fiyatını hesapladıktan sonra kullanıcıdan isim, TC kimlik
numarası, kredi kartı numarası ve kredi kartı şifresi istemektedir.
● Veritabanı olarak adlandırdığımız "Orders_Database.csv" dosyasında pizzasını
seçen ve kullanıcı adını, kullanıcı kimliğini, kredi kartı bilgilerini, sipariş açıklamasını,
sipariş zamanını ve kredi kartı şifresini tutan bir tablo oluşturunuz.
