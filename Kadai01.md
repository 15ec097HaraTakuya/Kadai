# 課題1  
ここではMATLABを用いて標本化間隔による解像度の違いを確認する。  
まず、MATLABに画像を読み込み表示する。  
読み込み用にimread関数を、表示用にimage(sc)関数を用いて以下の様に記述する。  
  
IMG = imread();%画像をIMG変数に格納  
image(IMG);%IMGを表示  
ここでは、次の縦533×800の画像を使う。  
![写真](https://github.com/15ec097HaraTakuya/Kadai/blob/master/Kimono.jpg)  
図1 使用原画像  
