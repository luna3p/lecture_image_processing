# �ۑ�8���|�[�g

https://www.pakutaso.com/20140657168post-4246.html �̃C���X�g�����摜�Ƃ���D���̉摜�͏c900�摜�C��1600��f�ɂ�钷���`�̃f�B�W�^���J���[�摜�ł���D

ORG=imread('cat.jpg'); % ���摜�̓���  
ORG = rgb2gray(ORG); colormap(gray); colorbar;  
imagesc(ORG); axis image; % �摜�̕\��

�ɂ���āC���摜���O���[�X�P�[���ǂݍ��݁C�\���������ʂ�}�P�Ɏ����D

![���摜](https://github.com/luna3p/lecture_image_processing/blob/master/image/image8_1.PNG?raw=true)  
�}1 ���摜

臒l�P�Q�W�œ�A�����s��. 臒l�P�Q�W�œ�A�����s�����摜��}�Q�Ɏ���. 

IMG = ORG>128; % 128�ɂ���l��
imagesc(IMG); colormap(gray); colorbar; % �摜�̕\��

![���摜](https://github.com/luna3p/lecture_image_processing/blob/master/image/image8_2.PNG?raw=true)  
�}2 臒l�P�Q�W�ł̓�A���摜

���ɓ�l�����ꂽ�摜�Ƀ��x����t����.���x�����O�Ƃ͓����A�������ɑ������f�ɓ���̔ԍ���^���鏈�����w��. 

IMG = bwlabeln(IMG);
imagesc(IMG); colormap(jet); colorbar; % �摜�̕\��

![���摜](https://github.com/luna3p/lecture_image_processing/blob/master/image/image8_3.PNG?raw=true)  
�}3 ���x�����O�摜

�}�R