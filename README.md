Iketahasi.csv
===

住居表示以前，以後の靜岡市の町丁名の對照表である． https://www.city.shizuoka.lg.jp/735_000001.html から作成した．

- `source.csv`: 上記 URL で配布の `.xls` から LibreOffice で CSV に變換し， header 行を削除したものである．
- `Iketahasi.csv`: 舊新の表．`cat source.csv | ruby -F, -ane 'puts $F[1]+","+$F[5]' | sort | uniq > Iketahasi.csv` で生成した．

- `Iketahasi_inverse.csv`: 新舊の表．`cat source.csv | ruby -F, -ane 'puts $F[5]+","+$F[1]' | sort | uniq > Iketahasi_inverse.csv` で生成した．
