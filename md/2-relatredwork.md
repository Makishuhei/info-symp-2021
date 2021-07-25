# 関連研究
この章では、今まで研究されてきた説明的可視化や時系列データに対する可視化をみていく。
<!-- Fig 1,2,3 -->

<!-- ![Figure 1: An example of applying the interactive Map Reports system to data on the number of deaths and storms per year by state in the United States.](img/1_iMR.png) -->
![Figure 1: interactive Map Reports](img/1_iMR.png)

Latifら[@latif2019interactive]は、二変量の地理統計データを理解するためにinteractive Map Reports(以下iMR)システムを開発し、説明的可視化を行っている。
地図上の行政区の色や行政区に関する統計量を表すグリフを使って二つの地理統計変数を可視化するとともに、データを解析して文章を自動生成しているのを、いくつかの例を上げながら説明している。
図1はその例の一つであり、アメリカ合衆国の各州の年間の死亡者数とハリケーンの発生数に対してiMRのシステムを使用したものである。
生成された文章には、「The average number of deaths per state was 14.9, ... (死亡者数の平均値が14.9万人だった。...)」などの統計的な特徴をはじめ、「Southern states faced higher number of deaths and storms compared to the other states..(南部の州は、他の州と比べて死亡者数やハリケーンの発生数が多い。)」など、特定の州のデータの特徴だけではなく、データの分布から見つかる地理的な偏りなどのデータの特徴も言葉で説明されている。
iMRでは文章生成を行うプロセスを自身で定義し、ユーザーの要望に合わせてパラメータを変更することで柔軟な文章を自動で生成している。
iMRは先で述べたようなデータの特徴を文章によって伝えることができるが、特徴が多い時にはシステムの画面からはみ出るほどの量の文章が生成されてしまい、ユーザーの負担になってしまう。

![Figure 2: SPIViewer](img/2_SPI_viewer.png)

Latifらが開発したiMRは二変数のみの地理統計量データに対応していたが、Hosokawaら[@hosokawa2020scalable]は2019年のSPIデータを使い、データ項目数が多く、多変数の地理的統計量のデータに対して説明的可視化を行うSPIViewerを開発した。
Hosokawaらはこのデータの特徴をユーザーに伝えるために、指標の階層性と国々の地理的階層を利用して文章を生成している。
図2のでは、「機会」という指標とその子孫の指標について北アフリカの国々とサブサハラアフリカの国々を比較して文章を生成している。
また、棒グラフを用いて一つの指標に対するデータの分布を表現したり、散布図を用いて二つの指標に対するデータの分布を比較したりすることができる。
SPIViewerはSPIデータの階層性を活用してデータの特徴を文章によって伝えているが、時系列データに対してはサポートしていない。

<!-- ![Figure 3: An example of applying Gapminder to trivariate geo-statistical data. The size of the bubble indicates the number of people infected with HIV.](img/3_Gapminder.png) -->
![Figure 3: Gapminder](img/3_Gapminder.png)

時系列データの特徴を伝えるために可視化を使った研究は複数存在する[@andrienko2020visual;@bryan2016temporal;@van1999cluster]。そのなかでRoslingら[@rosling2011health]は、データ項目数の多い二つの地理統計変数データを可視化するために、バブルチャートとアニメーションを用いたGapminderというシステムを開発した(図3)。
時間に沿って動くバブルの位置や位置の変化によって、世界各国の二つの統計量の変化を提供している。
しかしGapminderでは、どのデータの特徴に注目するかはユーザーに全て任されていた。
そこでLuら[@lu2020illustrating]は、Gapminderのアニメーションの中で注目すべきタイミングを抽出する研究を行った。
Luらは時系列データの変化の傾向が変化した期間をデータ解析から特定して、時間を表すバーの中にその期間を表示している。
RoslingやLuらの研究は、データを解析して誰かにデータの特徴を伝えるプレゼンテーションを目的にしているため、データの探索するためのサポートは行われていない。

本研究では、データ項目数の多い時系列データの特徴を可視化と文章にをユーザーに提示し、その後のデータの探索をサポートするシステムを設計する。
文章生成において、Latifらを参考にしてテンプレートベースで文章を生成する。
その時に文章の量が多くならないようにHosokawaらのようにデータの構造に注目して文章を生成する。
本研究では、SPIデータの国の地理的な階層性だけに注目して文章を生成しており、指標の階層性に注目した時系列データに対する文章生成は今後の研究課題とする。
また、Luらが行った手法を参考に時系列データを解析して、時系列データの特徴を説明する。
生成される文章の量を短くするために、解析する時系列データをユーザーの探索に合わせて選択する。