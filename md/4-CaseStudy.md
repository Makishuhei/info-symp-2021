# ケーススタディ
<!-- Fig 5,4,6,7,8,9 -->

この章では提案するシステムが三つの要件、**R1 時系列データの変化の特徴**,**R2 データの関係性から見た概要**,**R3 データ項目を絞ったデータの探索**を満たされていることを示す。

![Figure 5: An example of using the system with Personal Rights as the index, the Americas as the geographical area, and the United States as the country of interest. It can be seen from the line chart that the United States has the highest value of Personal Rights in the Americas, and that it has been gradually decreasing for 10 years. It can be also seen that there are countries in the Americas with high and low values of the index, and that there are many countries in North America with high values of the index among the Americas.](img/5_SPI_Time_Series.png)

図5は地理的範囲を「南北アメリカ」、指標を「個人の権利」、注目するデータ項目を「アメリカ合衆国」にした例である。
アメリカ合衆国は南北アメリカの中で最も個人の権利の値が高いこと、10年間徐々に減少していることが折れ線から読み取れる(**R1**)。
文章の地理的階層に直目した内容として、南北アメリカの国々は指標の値が高い国から低い国まで存在することや、南北アメリカの中で北アメリカには指標の値が高い国が多いことが書かれている(**R2**)。
これらのことは、折れ線のデータの分布を確認したり、選択する地理的範囲を北アメリカに変更したりすることで確認することができる。
次に注目する国に関しての内容で、アメリカ合衆国が南北アメリカの中で指標の値が高いことや、10年間緩やかに減少していることがわかる(**R3**)。
このことも折れ線のデータの変化や分布などから読み取ることができる。

![Figure 6: A comparison of data from Japan and Australia on access to information and communication shows that they are very similar.](img/6_SPI_Time_Series.png)

他の国や指標についてもみていく。
図4は地理的範囲を「世界」、指標を「情報通信へのアクセス」、注目するデータ項目を「日本」にしている。
先ほどと異なってわかる特徴として、2013年に指標の値の変化の傾向が変わったことが折れ線からわかる。
このとき、情報通信へのアクセスが伸びることは良いことなので、その上昇率が下がることはよくない変化として黒のドットに表されている。(**R1**)
他には、類似している国に、オーストラリアがあることがわかる。
類似していない国の表示を隠すと、日本とオーストラリアのデータは非常に似ていることが確認できる。(図6)
次に文章の方をみていく(図4右)。
先ほどと同様に世界の国々の中で、オセアニアには指標の値が低い国が多く、ヨーロッパには指標の値が高い国が多いことがわかる(**R2**)。
国の特徴として、日本は2011年から2013年にかけてこの指標が大きく上昇したことを文章からも確認できる。

![Figure 7a](img/7a_SPI_Time_Series.png)

![Figure 7b](img/7b_SPI_Time_Series.png)

![Figure 7c: An example where the indicator is personal safety and the geographic scope is Europe. The central figure in (a) shows that Russia has the lowest value for the indicator in Europe. In (b), the country of interest is Finland, and it can be seen that countries with similar data to Finland are clustered from west to north in Europe. Belgium, the only country in the west of Europe whose data was not similar to Finland's, showed a decrease in the value of the indicator from 2015 to 2016, as can be seen in the central figure in (c).](img/7c_SPI_Time_Series.png)

最後に別のアプローチでデータを探索していく。
図7aは地理的範囲を「ヨーロッパ」、指標を「個人の安全」とした例である。
まず折れ線をみるとデータが他のデータ項目より値が低いデータ項目があるのがわかる。
ホバーすると、それがロシアであることがわかる。
タップすると注目する国が「ロシア」に変わり、文章として詳細なデータの特徴を得ることができる。
文章から、やはりロシアは指標の値がヨーロッパの中で非常に低いことがわかる(図7a右)。
次にロシアと隣接している国は類似していない国ということから、それらの国データが気になる。
ロシアの北西に位置する「フィンランド」を地図から選択してみる(図7b)。
すると、ロシアとは異なりフィンランドは指標の値が高いことが折れ線の分布(図7b中央)からわかる。
また地図(図7左)より、フィンランドとデータが類似している国がヨーロッパの西から北に集まっていることがわかる(**R2**)。
しかし西側のベルギーという国は、フィンランドとデータが類似している国に含まれていない。
そこでベルギーのデータを見てみると、ベルギー2015年までは周辺諸国と同じような値をとっていたが、2016年で大きく減少していることがわかる(**R1**)。