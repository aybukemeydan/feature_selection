# Feature Selection

Elinizde her zaman az kolonlu ve heatmap üzerinden kolayca inceleyebildiğiniz bir data olmuyor. Kendiniz 1000 kolonlu bir havuz içerisinde bulabiliyorsunuz. Bunların hepsini de modele koymak size overfittingden başka bir sonuç getirmeyecektir de. O yüzden bu adım çok kritik.

### 1.) İsmail Parsa'nın Sunumundan Aldığım Notlar


<img src="feature_selection.png" width="1000px">

Solda sırasıyla feature seçmedeki adımlar bulunmakta.

1.) Min korelasyon thresholdu belirlenip (0,2 ya da 0,02 olabilir) bu eşik değerin altında olanlar atılır.

2.) Redundancy : Birbirine çok yakın featureları atmaca. 2 feature birbirine 0,85 oranında yakınsa targetla daha fazla korele olanı tut.

3.) Bootsrap Regression : Regresyon analizi kullanılarak resampling tekniği dediğimiz yani veriden 5 kere %40 gibi bir oranda (farklı oranlarda olabilir.) sample çekip 5 kere regresyon yapıp 5 i içinde 3 ünde önemli olmuş featurelarla devam etme.

4.) En sonda da modele sokup (3 defa) feature importance'ı en yüksek ortak değişkenlerle devam ederek final modeli kurmak.

Sağdaki grafikte 2 ayrı modelin AUC değerleri gözükmekte turuncu kısımda yukardaki adımların hepsi uygulanmış gri kısımda da yukardaki 1.adımdan sonrası yapılmamış. Lift curve'e bakınca iki model arasındaki fark gözükmekte.


### 2.)  Feature Selectionda Kullandığım Diğer Yöntemler

Özellikle AutoViz'i çok severek kullanıyorum,özellikle çok kolonlu (+700) bir data ile çalışıyorsanız yukarıdaki ilk 3 adımı sadece bu yolla kullanabilirsiniz. Yine featurewizz ile de pandas_profilling tadında grafikleri görebilir ve inceleyebilirsiniz. En sonunda heatmap çizdirmesiyle de tadından yenmiyor.
<br/>**📫 Linkler :** <br/>

* [DS Tutorial](https://github.com/edyoda/data-science-complete-tutorial/blob/master/10.%20Feature%20Selection%20Techniques.ipynb)
* [Drop Corr Features](https://github.com/feature-engine/feature-engine-examples/blob/main/selection/Drop-Correlated-Features.ipynb)
* [Redundancy](https://github.com/anujdutt9/Feature-Selection-for-Machine-Learning/blob/master/Filter%20Methods/Correlation.ipynb)
* [ABESS -Fast Best-Subset Selection in Python and R](https://github.com/abess-team/abess)
* [Featurewizz](https://github.com/AutoViML/featurewiz)
* [AutoViz - Demo](https://github.com/AutoViML/AutoViz/blob/master/Examples/AutoViz_Demo.ipynb)



