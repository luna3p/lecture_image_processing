# �ۑ�10���|�[�g

https://www.pakutaso.com/20140657168post-4246.html �̃C���X�g�����摜�Ƃ���D���̉摜�͏c900�摜�C��1600��f�ɂ�钷���`�̃f�B�W�^���J���[�摜�ł���D

ORG=imread('cat.jpg'); % ���摜�̓���  
ORG = rgb2gray(ORG); colormap(gray); colorbar;  
imagesc(ORG); axis image; % �摜�̕\��

�ɂ���āC���摜���O���[�X�P�[���ǂݍ��݁C�\���������ʂ�}�P�Ɏ����D

![���摜](https://github.com/luna3p/lecture_image_processing/blob/master/image/image10_1.PNG?raw=true)  
�}1 ���摜

�v���E�B�b�g�@�ŃG�b�W���o�����摜��}�Q�Ɏ���. 

IMG = edge(ORG,'prewitt');

![���摜](https://github.com/luna3p/lecture_image_processing/blob/master/image/image10_2.PNG?raw=true)  
�}2 �G�b�W���o�i�v���E�B�b�g�@�j

�\�x���@�ŃG�b�W���o�����摜��}�R�Ɏ���. 

IMG = edge(ORG,'sobel');

![���摜](https://github.com/luna3p/lecture_image_processing/blob/master/image/image10_3.PNG?raw=true)  
�}3 �G�b�W���o�i�\�x���@�j

�L���j�[�@�ŃG�b�W���o�����摜��}�S�Ɏ���. 

IMG = edge(ORG,'canny');

![���摜](https://github.com/luna3p/lecture_image_processing/blob/master/image/image10_4.PNG?raw=true)  
�}�S �G�b�W���o�i�L���j�[�@�j

�e�G�b�W���o�@�̉摜���m�F�����, �v���E�B�b�g�@�ƃ\�x���@�͂��܂�ω����Ȃ��ǂ�����֊s��������ɂ����Ȃ��Ă���. ����ɑ΂��L���j�[�@�͒��o������Ă���ӏ��������֊s��������ɂ����Ȃ��Ă���Ɍ�����. 
