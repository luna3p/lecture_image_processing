# �ۑ�6���|�[�g

https://www.pakutaso.com/20140657168post-4246.html �̃C���X�g�����摜�Ƃ���D���̉摜�͏c900�摜�C��1600��f�ɂ�钷���`�̃f�B�W�^���J���[�摜�ł���D

ORG=imread('cat.jpg'); % ���摜�̓���  
ORG = rgb2gray(ORG); colormap(gray); colorbar;  
imagesc(ORG); axis image; % �摜�̕\��

�ɂ���āC���摜���O���[�X�P�[���ǂݍ��݁C�\���������ʂ�}�P�Ɏ����D

![���摜](https://github.com/luna3p/lecture_image_processing/blob/master/image/image6_1.PNG?raw=true)  
�}1 ���摜

臒l�P�Q�W�œ�A�����s��. 臒l�P�Q�W�œ�A�����s�����摜��}�Q�Ɏ���. 

IMG = ORG>128; % 128�ɂ���l��
imagesc(IMG); colormap(gray); colorbar; % �摜�̕\��

![���摜](https://github.com/luna3p/lecture_image_processing/blob/master/image/image6_2.PNG?raw=true)  
�}2 臒l�P�Q�W�ł̓�A���摜

���Ƀf�B�U�@��p���ĉ摜�̓�A�����s��. �f�B�U�@��p���ē�A�����s�����摜��}�R�Ɏ����D

IMG = dither(ORG); % �f�B�U�@�ɂ���l��
imagesc(IMG); colormap(gray); colorbar; % �摜�̕\��

![���摜](https://github.com/luna3p/lecture_image_processing/blob/master/image/image6_3.PNG?raw=true)  
�}3 �f�B�U�@�ł̓�A���摜

�f�B�U�@��p�����臒l�P�Q�W�ł̓�A�摜���ח֊s���͂�����Ɗm�F�ł���. 
