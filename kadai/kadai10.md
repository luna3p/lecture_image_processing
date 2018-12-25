# 課題10レポート

https://www.pakutaso.com/20140657168post-4246.html のイラストを原画像とする．この画像は縦900画像，横1600画素による長方形のディジタルカラー画像である．

ORG=imread('cat.jpg'); % 原画像の入力  
ORG = rgb2gray(ORG); colormap(gray); colorbar;  
imagesc(ORG); axis image; % 画像の表示

によって，原画像をグレースケール読み込み，表示した結果を図１に示す．

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image10_1.PNG?raw=true)  
図1 原画像

プレウィット法でエッジ抽出した画像を図２に示す. 

IMG = edge(ORG,'prewitt');

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image10_2.PNG?raw=true)  
図2 エッジ抽出（プレウィット法）

ソベル法でエッジ抽出した画像を図３に示す. 

IMG = edge(ORG,'sobel');

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image10_3.PNG?raw=true)  
図3 エッジ抽出（ソベル法）

キャニー法でエッジ抽出した画像を図４に示す. 

IMG = edge(ORG,'canny');

![原画像](https://github.com/luna3p/lecture_image_processing/blob/master/image/image10_4.PNG?raw=true)  
図４ エッジ抽出（キャニー法）

各エッジ抽出法の画像を確認すると, プレウィット法とソベル法はあまり変化がなくどちらも輪郭が分かりにくくなっている. それに対しキャニー法は抽出視されている箇所が多く輪郭が分かりにくくなっているに見える. 
