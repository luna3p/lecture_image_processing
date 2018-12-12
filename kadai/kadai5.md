# 課題5レポート

https://www.pakutaso.com/20140657168post-4246.html のイラストを原画像とする．この画像は縦900画像，横1600画素による長方形のディジタルカラー画像である．

ORG=imread('cat.jpg'); % 原画像の入力  
ORG = rgb2gray(ORG); colormap(gray); colorbar;  
imagesc(ORG); axis image; % 画像の表示

によって，原画像をグレースケール読み込み，表示した結果を図１に示す．

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image5_1.PNG?raw=true)  
図1 原画像

原画像の判別分析法を用いて二植化を行う. 判別分析法とは対象物の濃度と背景の濃度とがそれぞれ最もよくまとまり, かつ
対象物と背景の違いが区別できるような閾値を決める方法である. まず全画素の濃度の平均値を求める. 次に濃度tでクラスを分け, その２つの
クラスの分散, 平均値, 画素数を求める. クラス内分散とクラス間分散を求める.クラス間分散の二乗をクラス内分散の二乗で割り, その値が最大となるような濃度tを求める. 


C1 = H(1:i); %ヒストグラムを2つのクラスに分ける  
C2 = H(i+1:256);  
n1 = sum(C1); %画素数の算出  
n2 = sum(C2);  
myu1 = mean(C1); %平均値の算出  
myu2 = mean(C2);  
sigma1 = var(C1); %分散の算出  
sigma2 = var(C2);  
sigma_w = (n1 *sigma1+n2*sigma2)/(n1+n2); %クラス内分散の算出  
sigma_B = (n1 *(myu1-myu_T)^2+n2*(myu2-myu_T)^2)/(n1+n2); %クラス間分散の算出  
if max_val<sigma_B/sigma_w  
max_val = sigma_B/sigma_w;  
max_thres =i;  

判別分析法を用いて二植化を行った画像を図２に示す. 

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image5_2.PNG?raw=true)  
図2 判別分析法による二植化画像


この二値画像の閾値の値は

disp(max_thres);

によって参照でき, 閾値は９８となった. 
