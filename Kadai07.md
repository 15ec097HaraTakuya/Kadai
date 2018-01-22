# 課題7　ダイナミックレンジの拡大  
ここでは、画像のダイナミックレンジを拡大する処理を確認する。  
  課題2同様、白黒画像を用いる為次のコードを記述する。  
  
>> ORG = imread('Nuko.jpg');  
>> ORG= rgb2gray(ORG);  
>> imagesc(ORG); colormap(gray); colorbar;  
>> pause;  
  
![Alt text](MATLAB/kadai7/Nuko1.jpg)  
図1 白黒画像  
  
次に濃度ヒストグラムを作成する。  
  
>> imhist(ORG);  
pause;  
  
![Alt text](MATLAB/kadai7/Nuko2.jpg)  
図2 濃度ヒストグラム  
  
そして、ダイナミックレンジを拡大のため次のコードを記述する。  
  
>> ORG = double(ORG);  
mn = min(ORG(:)); %   
mx = max(ORG(:)); %   
ORG = (ORG-mn)/(mx-mn)*255;  
imagesc(ORG); colormap(gray); colorbar;  
pause;  
>> ORG = uint8(ORG); %0~255の整数でダイナミックレンジを表現するためには、8ビットの符号なし整数に変換する必要があり、その為uint8型を用いてキャストする。  
imhist(ORG);  
  
結果を図3,4に示す。
![Alt text](MATLAB/kadai7/Nuko3.jpg)  
図3 ダイナミックレンジ拡大画像  
![Alt text](MATLAB/kadai7/Nuko4.jpg)  
図4 ダイナミックレンジ拡大後の濃度ヒストグラム  
  
