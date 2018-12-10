# 課題3レポート

https://www.pakutaso.com/20140657168post-4246.html のイラストを原画像とする．この画像は縦900画像，横1600画素による長方形のディジタルカラー画像である．

ORG=imread('cat.jpg'); % 原画像の入力  
ORG = rgb2gray(ORG); colormap(gray); colorbar;  
imagesc(ORG); axis image; % 画像の表示

によって，原画像をグレースケール読み込み，表示した結果を図１に示す．

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image3_1.PNG?raw=true)  
図1 原画像

原画像の4つの閾値(６４, ９６, １２８, １９２)で閾値処理した画像の表示を行う. 輝度値６４を閾値とする場合, ６４以上の画像を１, その他を０に変換して表示する. 

IMG = ORG > 64;

輝度値が６４の結果を図２に示す．

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image3_2.PNG?raw=true)  
図2 輝度値６４での閾値処理

同様に輝度値９６を閾値として閾値処理を行う.

IMG = ORG > 96;

閾値が９６の結果を図３に示す．

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image3_3.PNG?raw=true)  
図3 輝度値９６の閾値処理
              
輝度値128, 192を閾値として閾値処理を行う. 

閾値が１２８の結果を図４に示す．

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image3_4.PNG?raw=true)  
図4 輝度値１２８の閾値処理

閾値が１９２の結果を図４に示す．

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image3_5.PNG?raw=true)  
図4 輝度値１９２の閾値処理

このように閾値とする輝度値が大きくなると，黒の画素が目立つようになる．
