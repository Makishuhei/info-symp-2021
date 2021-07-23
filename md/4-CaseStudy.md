# ケーススタディ
<!-- Fig 5,4,6,7,8,9 -->

この章では提案するシステムを使って四つの要件、**R1: 変化の特定, R2: 階層的な情報, R3: 地理的範囲の表示, R4: 概要**が満たされているかを確認していく。

![Figure 5: An example of using the system with Personal Rights as the index, the Americas as the geographical area, and the United States as the country of interest. It can be seen from the line chart that the United States has the highest value of Personal Rights in the Americas, and that it has been gradually decreasing for 10 years. It can be also seen that there are countries in the Americas with high and low values of the index, and that there are many countries in North America with high values of the index among the Americas.](img/5_SPI_Time_Series.png)

図5は地理的範囲を**南北アメリカ**、指標を**個人の権利**、注目する国を**アメリカ合衆国**にしている。
折れ線からはアメリカ合衆国は南北アメリカの中で最も個人の権利という指標がの値が高いこと、10年間徐々に減少していることがわかる。
またこのとき南北アメリカ内でアメリカ合衆国と類似した動向をした国はなかった。
文章の方をみていく。(**文章1**)
南北アメリカの国々は指標の値が高い国から低い国まで存在することがわかる。
確かに折れ線を確認すると指標の高い国が多いことがすぐにわかるが、キューバが他の国と比べて極端に低い値をとっていることがわかる。
また、南北アメリカの中で北アメリカには指標の値が高い国が多いことがわかる(**R2**)。
このことは選択する地理的範囲を北アメリカに変更すると確認することができる。
次にアメリカが南北アメリカの中で指標の値が高いことや、10年間緩やかに減少していることがわかる。(**R4**)

![Figure 6: A comparison of data from Japan and Australia on access to information and communication shows that they are very similar.](img/6_SPI_Time_Series.png)

他の国や指標についてもみていく。
図4は地理的範囲を**世界**、指標を**情報通信へのアクセス**、注目する国を**日本**にしている。
先ほどと異なってわかる情報として、2013年に指標の値の変化の傾向が変わったことが折れ線からわかる(**R1**)。
こととき、情報通信へのアクセスが伸びることは良いことなので、その上昇率が下がることはよくない変化として黒塗りでドットに表されている。
他にはわかる情報として、似たような動向をしている国に、オーストラリアがあることがわかる。
類似していない国の表示を隠すと、日本とオーストラリアのデータは非常に似ていることが確認できる。(図6)
次に文章の方をみていく(**文章2**)。
先ほどと同様に世界の国々の中で、オセアニアには指標の値が低い国が多く、ヨーロッパには指標の値が高い国が多いことがわかる。
国の情報として、日本は2011年から2013年にかけてこの指標が大きく上昇したことを文章からも確認できる。

![Figure 7a:](img/7a_SPI_Time_Series.png)

![Figure 7b:](img/7b_SPI_Time_Series.png)

![Figure 7c:](img/7c_SPI_Time_Series.png)

最後に別のアプローチでデータを探索していく。
指標を**個人の安全**とし地理的範囲を**ヨーロッパ**とする。
まず折れ線をみると一番データの値が低い国があるのがわかる。
ホバーするとそれがロシアであることがわかり、タップしてみると注目する国が**ロシア**になり、文章として詳細な情報を得ることができる。
文章から、やはりロシアは指標の値がヨーロッパの中で非常に低いことがわかる(**文章3**)。
次にロシアと隣接している国の指標の値が気になり、ロシアの北西に位置する**フィンランド**を地図から選択してみる。
するとフィンランドはロシアとは異なり、指標の値が高いことがわかる。
また地図より、フィンランドと値が近くデータの変動が似ている国がヨーロッパの西から北に固まっていることがわかった(**R3**)。
一方、西側のベルギーという国はフィンランドと値が近くデータの変動が似ている国に含まれていない。
そこでベルギーを地図から選択すると、ベルギー2015年までは周辺諸国と同じような値をとっていたが、2016年で大きく減少していることがわかる。**図**