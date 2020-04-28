# gakusei_soudan
学生相談週間のためのスクリプトです。

 - スクリプトは現在作成中です。
 

# 必要な環境
- Python 2
- pandas

# スクリプトの仕様と利用手順

## 指導教員に配布するファイルを作成しましょう。
1. 教務係から学生情報のCSVをもらう
2. もらったCSVを指定して、スクリプトを実行する。 `python make_sidou_kyouin_file.py --input <教務係からもらったCSVファイル> --output <出力ディレクトリ>'
3. 指定した出力ディレクトリに、教員ごとにエクセルファイルが作成される。（教員の人数の分だけファイルが複数作られる）

### 作成されるエクセルファイルの仕様

#### ファイル名

`相談週間_<指導教員名>.xlsx`

**指導教員名はスペースが除外されます。**

#### 作成されるエクセルファイルの中身（CSV形式で表現）

```
学科,学年,学籍番号,カタカナ氏名,学生氏名,指導教員,在籍状況,評価,詳細報告_コメント
XX学科,1,1234,スズキイチロウ,鈴木一朗,(指導教員名), 1234,在学中,（ブランク）,（ブランク）
YY学科,3,3234,イソノサザエ,磯野サザエ,(指導教員名), 1234,休学中,（ブランク）,（ブランク）
```

学年でソートされる（はず）です。

## 作成されたファイルを学内サーバーにアップロードしましょう

学内サーバーに関する問い合わせはサポートいたしません。

## 指導教員から提出されたエクセルファイルのマージをしましょう。

1. 提出されたファイルを特定のディレクトリに格納する
2. そのディレクトリを指定して、スクリプトを実行する。 `python merge_sidou_kyouin_file.py --input <格納したディレクトリ> --output <出力ディレクトリ>'
3. 指定した出力ディレクトリに、マージされたエクセルファイルが一つ作成される。

## マージしたファイルを委員会で確認しましょう。

みんな元気だと良いですね！
