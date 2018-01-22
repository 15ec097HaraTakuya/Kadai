# 課題2　階調数と疑似輪郭  
ここでは使用画像Kimono.jpgのグレースケールに対し  
２階調，４階調，８階調の画像を生成する。 
そのためまず、以下のコードを記述する。  
  
ORG = imread('Kimono.jpg');%画像をIMG変数に格納  
IMG = rgb2gray(ORG); colormap(gray); colorbar;  
imagesc(IMG); axis image; % 画像の表示  
pause; % 一時停止  
  
使用原画像のグレースケールを図1に示す。  
  
  
図1 グレースケール  
  
## 2階調  
2階調画像作成のため次のコードを記述する。  
  
IMG2 = IMG>128;  
imagesc(IMG2); colormap(gray); colorbar;  axis image;  
pause;  
  
2階調画像を図2に示す。  
  

  
図2 二階調画像  
  
## 4階調
