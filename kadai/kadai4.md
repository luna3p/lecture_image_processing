# 課題4レポート

https://www.pakutaso.com/20140657168post-4246.html のイラストを原画像とする．この画像は縦900画像，横1600画素による長方形のディジタルカラー画像である．

ORG=imread('cat.jpg'); % 原画像の入力  
ORG = rgb2gray(ORG); colormap(gray); colorbar;  
imagesc(ORG); axis image; % 画像の表示  

によって，原画像をグレースケール読み込み，表示した結果を図１に示す．

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image4_1.PNG?raw=true)  
図1 原画像

原画像のヒストグラムの作成を行う. 

imhist(ORG);

横軸を輝度値の値, 縦軸をその輝度値の画素数としてヒストグラムを作成しそのヒストグラムを図２に示す．

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image4_2.PNG?raw=true)  
図2 ヒストグラム


ヒストグラム化するとその画像の輝度値の分布がわかる．
