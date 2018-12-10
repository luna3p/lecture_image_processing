# 課題4レポート

https://www.pakutaso.com/20140657168post-4246.html のイラストを原画像とする．この画像は縦900画像，横1600画素による長方形のディジタルカラー画像である．

ORG=imread('cat.jpg'); % 原画像の入力  
ORG = rgb2gray(ORG); colormap(gray); colorbar;  
imagesc(ORG); axis image; % 画像の表示

によって，原画像をグレースケール読み込み，表示した結果を図１に示す．

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image4_1.PNG?raw=true)  
図1 原画像

原画像の判別分析法を用いて二植化を行う. 判別分析法とは対象物の濃度と背景の濃度とがそれぞれ最もよくまとまり, かつ
対象物と背景の違いが区別できるような閾値を決める方法である. まず全画素の濃度の平均値を求める. 次に濃度tでクラスを分け, その２つのクラスの分散, 平均値, 画素数を求める. クラス内分散とクラス間分散を求める. 
$$
\frac{\sigma {_{B}}^{2}}{\sigma {_{\omega }}^{2}}
$$
が最大となるような濃度tを求める. 


imhist(ORG);

横軸を輝度値の値, 縦軸をその輝度値の画素数としてヒストグラムを作成しそのヒストグラムを図２に示す．

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image4_2.PNG?raw=true)  
図2 ヒストグラム


ヒストグラム化するとその画像の輝度値の分布がわかる．
