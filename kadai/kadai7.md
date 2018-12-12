# 課題7レポート

https://www.pakutaso.com/20180839213post-16954.htmlのイラストを原画像とする．この画像は縦852画像，横1280画素による長方形のディジタルカラー画像である．

ORG=imread('cat.jpg'); % 原画像の入力  
ORG = rgb2gray(ORG); colormap(gray); colorbar;  
imagesc(ORG); axis image; % 画像の表示

によって，原画像をグレースケール読み込み，表示した結果を図１に示す．

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image7_1.PNG?raw=true)  
図1 原画像

原画像のヒストグラムの作成を行う. 

imhist(ORG);

横軸を輝度値の値, 縦軸をその輝度値の画素数としてヒストグラムを作成しそのヒストグラムを図２に示す．

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image7_2.PNG?raw=true)  
図2 原画像のヒストグラム

図２のヒストグラムを観察すると輝度値０～７０程の値が使用できていないことが分かる. この画像のレンジを広げるための処理を行う. 

ORG = double(ORG);
mn = min(ORG(:)); % 濃度値の最小値を算出
mx = max(ORG(:)); % 濃度値の最大値を算出
ORG = (ORG-mn)/(mx-mn)*255;
imagesc(ORG); colormap(gray); colorbar; % 画像の表示

ダイナミックレンジを拡大したときの画像を図３に示す. 

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image7_3.PNG?raw=true)  
図3 ダイナミックレンジ拡大後の画像

図３の画像のヒストグラムの作成を行う. 

ORG = uint8(ORG); % この行について考察せよ
imhist(ORG); % 濃度ヒストグラムを生成、表示

によってヒストグラムを表示できる. uint8(ORG)はダイナミックレンジの拡大のためにORGを一度double型に型変換を行っている. この画像は０～２５５の
８ビット画像なので８ビット符号なし整数配列に変換しなおす必要がある. そのためuint8(ORG)の処理を行っている.  
図４にダイナミックレンジ拡大後の画像のヒストグラムを示す. 

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image7_4.PNG?raw=true)  
図4 ダイナミックレンジ拡大後のヒストグラム
