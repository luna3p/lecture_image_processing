# �ۑ�7���|�[�g

https://www.pakutaso.com/20180839213post-16954.html�̃C���X�g�����摜�Ƃ���D���̉摜�͏c852�摜�C��1280��f�ɂ�钷���`�̃f�B�W�^���J���[�摜�ł���D

ORG=imread('cat.jpg'); % ���摜�̓���  
ORG = rgb2gray(ORG); colormap(gray); colorbar;  
imagesc(ORG); axis image; % �摜�̕\��

�ɂ���āC���摜���O���[�X�P�[���ǂݍ��݁C�\���������ʂ�}�P�Ɏ����D

![���摜](https://github.com/luna3p/lecture_image_processing/blob/master/image/image7_1.PNG?raw=true)  
�}1 ���摜

���摜�̃q�X�g�O�����̍쐬���s��. 

imhist(ORG);

�������P�x�l�̒l, �c�������̋P�x�l�̉�f���Ƃ��ăq�X�g�O�������쐬�����̃q�X�g�O������}�Q�Ɏ����D

![���摜](https://github.com/luna3p/lecture_image_processing/blob/master/image/image7_2.PNG?raw=true)  
�}2 ���摜�̃q�X�g�O����

�}�Q�̃q�X�g�O�������ώ@����ƋP�x�l�O�`�V�O���̒l���g�p�ł��Ă��Ȃ����Ƃ�������. ���̉摜�̃����W���L���邽�߂̏������s��. 

ORG = double(ORG);
mn = min(ORG(:)); % �Z�x�l�̍ŏ��l���Z�o
mx = max(ORG(:)); % �Z�x�l�̍ő�l���Z�o
ORG = (ORG-mn)/(mx-mn)*255;
imagesc(ORG); colormap(gray); colorbar; % �摜�̕\��

�_�C�i�~�b�N�����W���g�債���Ƃ��̉摜��}�R�Ɏ���. 

![���摜](https://github.com/luna3p/lecture_image_processing/blob/master/image/image7_3.PNG?raw=true)  
�}3 �_�C�i�~�b�N�����W�g���̉摜

�}�R�̉摜�̃q�X�g�O�����̍쐬���s��. 

ORG = uint8(ORG); % ���̍s�ɂ��čl�@����
imhist(ORG); % �Z�x�q�X�g�O�����𐶐��A�\��

�ɂ���ăq�X�g�O������\���ł���. uint8(ORG)�̓_�C�i�~�b�N�����W�̊g��̂��߂�ORG����xdouble�^�Ɍ^�ϊ����s���Ă���. ���̉摜�͂O�`�Q�T�T��
�W�r�b�g�摜�Ȃ̂łW�r�b�g�����Ȃ������z��ɕϊ����Ȃ����K�v������. ���̂���uint8(ORG)�̏������s���Ă���.  
�}�S�Ƀ_�C�i�~�b�N�����W�g���̉摜�̃q�X�g�O����������. 

![���摜](https://github.com/luna3p/lecture_image_processing/blob/master/image/image7_4.PNG?raw=true)  
�}4 �_�C�i�~�b�N�����W�g���̃q�X�g�O����
