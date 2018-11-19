# ‰Û‘è2ƒŒƒ|[ƒg

https://www.pakutaso.com/20140657168post-4246.html ‚ÌƒCƒ‰ƒXƒg‚ğŒ´‰æ‘œ‚Æ‚·‚éD‚±‚Ì‰æ‘œ‚Íc900‰æ‘œC‰¡1600‰æ‘f‚É‚æ‚é’·•ûŒ`‚ÌƒfƒBƒWƒ^ƒ‹ƒJƒ‰[‰æ‘œ‚Å‚ ‚éD

ORG=imread('cat.jpg'); % Œ´‰æ‘œ‚Ì“ü—Í
ORG = rgb2gray(ORG); colormap(gray); colorbar;
imagesc(ORG); axis image; % ‰æ‘œ‚Ì•\¦

‚É‚æ‚Á‚ÄCŒ´‰æ‘œ‚ğƒOƒŒ[ƒXƒP[ƒ‹“Ç‚İ‚İC•\¦‚µ‚½Œ‹‰Ê‚ğ}‚P‚É¦‚·D

![Œ´‰æ‘œ](https://github.com/luna3p/lecture_image_processing/blob/master/image/image2_1.PNG?raw=true)  
}1 Œ´‰æ‘œ

Œ´‰æ‘œ‚Ì“ñŠK’²‰æ‘œ‚ğ•\¦‚·‚é‚É‚ÍC”’•”Z’W‚Ì•ªŠ„”‚ğ‚P‚É‚·‚ê‚Î‚æ‚¢D‚WƒrƒbƒgƒOƒŒ[ƒXƒP[ƒ‹‚Í‚O`‚Q‚T‚T‚È‚Ì‚Å‚»‚Ì”¼•ª‚Ì’l‚Å‚ ‚é‚P‚Q‚W‚æ‚è¬‚³‚¢‚©‘å‚«‚¢‚©‚Å•\¦‚·‚éD

IMG = ORG>128;

‚QŠK’²‰»‚ÌŒ‹‰Ê‚ğ}‚Q‚É¦‚·D

![Œ´‰æ‘œ](https://github.com/luna3p/lecture_image_processing/blob/master/image/image2_2.PNG?raw=true)  
}2 ‚QŠK’²

“¯—l‚ÉŒ´‰æ‘œ‚ÌlŠK’²‰æ‘œ‚ğ•\¦‚·‚é‚É‚ÍC”’•”Z’W‚Ì•ªŠ„”‚ğ‚R‚É‚·‚ê‚Î‚æ‚¢D•ªŠ„‚ÍC‚O`‚Q‚T‚T‚Ì‚P/‚S, ‚Q/‚S, ‚R/‚S ‚Å‚ ‚é‚U‚SC‚P‚Q‚W, ‚P‚X‚Q‚Ås‚¤D

IMG0 = ORG>64;
IMG1 = ORG>128;
IMG2 = ORG>192;
IMG = IMG0 + IMG1 + IMG2;

‚SŠK’²‰»‚ÌŒ‹‰Ê‚ğ}‚R‚É¦‚·D

![Œ´‰æ‘œ](https://github.com/luna3p/lecture_image_processing/blob/master/image/image2_3.PNG?raw=true)  
}3 ‚SŠK’²

1/8‚ÍC“¯—l‚É•ªŠ„”‚ğ‚V(‚R‚QC‚U‚SC‚X‚U, ‚P‚Q‚W, ‚P‚U‚OC‚P‚X‚Q, ‚Q‚Q‚W)‚Ås‚¤D

IMG0 = ORG>32;
IMG1 = ORG>64;
IMG2 = ORG>96;
IMG3 = ORG>128;
IMG4 = ORG>160;
IMG5 = ORG>192;
IMG6 = ORG>228;
IMG = IMG0 + IMG1 + IMG2 + IMG3 + IMG4 + IMG5 + IMG6;


‚WŠK’²‰»‚ÌŒ‹‰Ê‚ğ}‚S‚É¦‚·D
![Œ´‰æ‘œ](https://github.com/luna3p/lecture_image_processing/blob/master/image/image2_4.PNG?raw=true)  
}4 ‚WŠK’²

‚±‚Ì‚æ‚¤‚ÉŠK’²”‚ª‘å‚«‚­‚È‚é‚ÆC—×Ú‚·‚é‰æ‘fŠÔ‚ÌF‚Ì”Z“x‚Ì’i·‚ªŒ¸‚è, ŠŠ‚ç‚©‚³‚ª¶‚Ü‚ê‚éD