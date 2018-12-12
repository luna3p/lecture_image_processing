# 課題6レポート

https://www.pakutaso.com/20140657168post-4246.html のイラストを原画像とする．この画像は縦900画像，横1600画素による長方形のディジタルカラー画像である．

ORG=imread('cat.jpg'); % 原画像の入力  
ORG = rgb2gray(ORG); colormap(gray); colorbar;  
imagesc(ORG); axis image; % 画像の表示

によって，原画像をグレースケール読み込み，表示した結果を図１に示す．

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image6_1.PNG?raw=true)  
図1 原画像

閾値１２８で二植化を行う. 閾値１２８で二植化を行った画像を図２に示す. 

IMG = ORG>128; % 128による二値化  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image6_2.PNG?raw=true)  
図2 閾値１２８での二植化画像

次にディザ法を用いて画像の二植化を行う. ディザ法を用いて二植化を行った画像を図３に示す．

IMG = dither(ORG); % ディザ法による二値化  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image6_3.PNG?raw=true)  
図3 ディザ法での二植化画像

ディザ法を用いると閾値１２８での二植画像を比べ輪郭がはっきりと確認できる. 
