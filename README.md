# titanic analysis
タイタニック号乗客の生存予測

# 方針
- 欠損地の埋め方を工夫する。
    Pclassごとの平均で埋めるとか。
- モデルのパラメータのチューニング
    DNN以外ならGridSearchCVを使って汎化性能測るのがよさげ。
- 外れ値の扱い方。消すのか残すのか。

# 概要
- PassengerID:　乗客ID
- Survived: 　　生存結果 (1: 生存, 2: 死亡)　
- Pclass: 　　　乗客の階級 1が一番位が高いそう
- Name: 　　 　乗客の名前
- Sex: 　　　　 性別
- Age: 　　　　 年齢
- SibSp 　　 　 兄弟、配偶者の数。
- Parch 　　　　両親、子供の数。
- Ticket 　　　 チケット番号。
- Fare 　　　　 乗船料金。
- Cabin 　　　　部屋番号
- Embarked 　　 乗船した港　Cherbourg、Queenstown、Southamptonの３種

これらを利用してSurvivedのラベルを予測する。
