# �ۑ�8���|�[�g

https://www.pakutaso.com/20140657168post-4246.html �̃C���X�g�����摜�Ƃ���D���̉摜�͏c900�摜�C��1600��f�ɂ�钷���`�̃f�B�W�^���J���[�摜�ł���D

ORG=imread('cat.jpg'); % ���摜�̓���  
ORG = rgb2gray(ORG); colormap(gray); colorbar;  
imagesc(ORG); axis image; % �摜�̕\��

�ɂ���āC���摜���O���[�X�P�[���ǂݍ��݁C�\���������ʂ�}�P�Ɏ����D

![���摜](https://github.com/luna3p/lecture_image_processing/blob/master/image/image9_1.PNG?raw=true)  
�}1 ���摜

�m�C�Y�Y�t�����摜��}�Q�Ɏ���. 

ORG = imnoise(ORG,'salt & pepper',0.02);

![���摜](https://github.com/luna3p/lecture_image_processing/blob/master/image/image9_2.PNG?raw=true)  
�}2 �m�C�Y�Y�t�摜

�������t�B���^�ŎG���������s�����摜��}�R�Ɏ���. 

IMG = filter2(fspecial('average',3),ORG);

![���摜](https://github.com/luna3p/lecture_image_processing/blob/master/image/image9_3.PNG?raw=true)  
�}3 ���x�����O�摜

���f�B�A���t�B���^�ŎG���������s�����摜��}�S�Ɏ���. 

IMG = medfilt2(ORG,[3 3]);

![���摜](https://github.com/luna3p/lecture_image_processing/blob/master/image/image9_4.PNG?raw=true)  
�}�S ���x�����O�摜

�݌v�����t�B���^��}�T�Ɏ���. 

f=[0,-1,0;-1,5,-1;0,-1,0]; % �t�B���^�̐݌v
IMG = filter2(f,IMG,'same'); % �t�B���^�̓K�p

![���摜](https://github.com/luna3p/lecture_image_processing/blob/master/image/image9_5.PNG?raw=true)  
�}�T �t�B���^�摜
