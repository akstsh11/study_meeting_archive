『Pythonによる機械学習入門 7章 センサーデータによる回帰問題』サンプルコードについて。
2016-11-28 ISP

[使い方]
・データファイル（CSVファイル）はスクリプトと同じフォルダに置いてください。
・コードの実行は以下のように行います。

  #コマンドラインの場合
  python スクリプト名

  # IPythonを含むpythonコンソールの場合は以下のように実行します。
  run スクリプト名

・7-5-2以降のスクリプトの実行には時間がかかります。


[修正箇所]
・P183
  2行目  dt.を削除
  誤：tmp['day'] = tmp.index.dt.day
  ↓
  正：tmp['day'] = tmp.index.day

・P180
  21行目 fillnaでinplace=True指定を追加

  誤：tmp["sunhour"].fillna(-1)
  ↓
  正：tmp["sunhour"].fillna(-1,inplace=True)

・P184
  最後、図7.8を出力するコードは7-5-3-2-graph.pyではなく7-5-5-4-graph.pyの誤りです。また、プロット対象に学習データを含めてしまっていますので図7-8も若干異なります。



以上