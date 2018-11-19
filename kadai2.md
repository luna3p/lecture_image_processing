# 課題2レポート

https://www.pakutaso.com/20140657168post-4246.html のイラストを原画像とする．この画像は縦900画像，横1600画素による長方形のディジタルカラー画像である．

ORG=imread('cat.jpg'); % 原画像の入力
ORG = rgb2gray(ORG); colormap(gray); colorbar;
imagesc(ORG); axis image; % 画像の表示

によって，原画像をグレースケール読み込み，表示した結果を図１に示す．

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image2_1.PNG?raw=true)  
図1 原画像

原画像の二階調画像を表示するには，白黒濃淡の分割数を１にすればよい．８ビットグレースケールは０～２５５なのでその半分の値である１２８より小さいか大きいかで表示する．

IMG = ORG>128;

２階調化の結果を図２に示す．

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image2_2.PNG?raw=true)  
図2 ２階調

同様に原画像の四階調画像を表示するには，白黒濃淡の分割数を３にすればよい．分割は，０～２５５の１/４, ２/４, ３/４ である６４，１２８, １９２で行う．

IMG0 = ORG>64;
IMG1 = ORG>128;
IMG2 = ORG>192;
IMG = IMG0 + IMG1 + IMG2;

４階調化の結果を図３に示す．

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image2_3.PNG?raw=true)  
図3 ４階調

1/8は，同様に分割数を７(３２，６４，９６, １２８, １６０，１９２, ２２８)で行う．

IMG0 = ORG>32;
IMG1 = ORG>64;
IMG2 = ORG>96;
IMG3 = ORG>128;
IMG4 = ORG>160;
IMG5 = ORG>192;
IMG6 = ORG>228;
IMG = IMG0 + IMG1 + IMG2 + IMG3 + IMG4 + IMG5 + IMG6;


８階調化の結果を図４に示す．

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image2_4.PNG?raw=true)  
図4 ８階調

このように階調数が大きくなると，隣接する画素間の色の濃度の段差が減り, 滑らかさが生まれる．
