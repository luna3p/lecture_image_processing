# �ۑ�2���|�[�g

https://www.pakutaso.com/20140657168post-4246.html �̃C���X�g�����摜�Ƃ���D���̉摜�͏c900�摜�C��1600��f�ɂ�钷���`�̃f�B�W�^���J���[�摜�ł���D

ORG=imread('cat.jpg'); % ���摜�̓���
ORG = rgb2gray(ORG); colormap(gray); colorbar;
imagesc(ORG); axis image; % �摜�̕\��

�ɂ���āC���摜���O���[�X�P�[���ǂݍ��݁C�\���������ʂ�}�P�Ɏ����D

![���摜](https://github.com/luna3p/lecture_image_processing/blob/master/image/image2_1.PNG?raw=true)  
�}1 ���摜

���摜�̓�K���摜��\������ɂ́C�����Z�W�̕��������P�ɂ���΂悢�D�W�r�b�g�O���[�X�P�[���͂O�`�Q�T�T�Ȃ̂ł��̔����̒l�ł���P�Q�W��菬�������傫�����ŕ\������D

IMG = ORG>128;

�Q�K�����̌��ʂ�}�Q�Ɏ����D

![���摜](https://github.com/luna3p/lecture_image_processing/blob/master/image/image2_2.PNG?raw=true)  
�}2 �Q�K��

���l�Ɍ��摜�̎l�K���摜��\������ɂ́C�����Z�W�̕��������R�ɂ���΂悢�D�����́C�O�`�Q�T�T�̂P/�S, �Q/�S, �R/�S �ł���U�S�C�P�Q�W, �P�X�Q�ōs���D

IMG0 = ORG>64;
IMG1 = ORG>128;
IMG2 = ORG>192;
IMG = IMG0 + IMG1 + IMG2;

�S�K�����̌��ʂ�}�R�Ɏ����D

![���摜](https://github.com/luna3p/lecture_image_processing/blob/master/image/image2_3.PNG?raw=true)  
�}3 �S�K��

1/8�́C���l�ɕ��������V(�R�Q�C�U�S�C�X�U, �P�Q�W, �P�U�O�C�P�X�Q, �Q�Q�W)�ōs���D

IMG0 = ORG>32;
IMG1 = ORG>64;
IMG2 = ORG>96;
IMG3 = ORG>128;
IMG4 = ORG>160;
IMG5 = ORG>192;
IMG6 = ORG>228;
IMG = IMG0 + IMG1 + IMG2 + IMG3 + IMG4 + IMG5 + IMG6;


�W�K�����̌��ʂ�}�S�Ɏ����D
![���摜](https://github.com/luna3p/lecture_image_processing/blob/master/image/image2_4.PNG?raw=true)  
�}4 �W�K��

���̂悤�ɊK�������傫���Ȃ�ƁC�אڂ����f�Ԃ̐F�̔Z�x�̒i��������, ���炩�������܂��D