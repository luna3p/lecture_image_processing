# 課題8レポート

https://www.pakutaso.com/20140657168post-4246.html のイラストを原画像とする．この画像は縦900画像，横1600画素による長方形のディジタルカラー画像である．

ORG=imread('cat.jpg'); % 原画像の入力  
ORG = rgb2gray(ORG); colormap(gray); colorbar;  
imagesc(ORG); axis image; % 画像の表示

によって，原画像をグレースケール読み込み，表示した結果を図１に示す．

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image9_1.PNG?raw=true)  
図1 原画像

ノイズ添付した画像を図２に示す. 

ORG = imnoise(ORG,'salt & pepper',0.02);

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image9_2.PNG?raw=true)  
図2 ノイズ添付画像

平滑化フィルタで雑音除去を行った画像を図３に示す. 

IMG = filter2(fspecial('average',3),ORG);

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image9_3.PNG?raw=true)  
図3 ラベリング画像

メディアンフィルタで雑音除去を行った画像を図４に示す. 

IMG = medfilt2(ORG,[3 3]);

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image9_4.PNG?raw=true)  
図４ ラベリング画像

設計したフィルタを図５に示す. 

f=[0,-1,0;-1,5,-1;0,-1,0]; % フィルタの設計  
IMG = filter2(f,IMG,'same'); % フィルタの適用

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image9_5.PNG?raw=true)  
図５ フィルタ画像
