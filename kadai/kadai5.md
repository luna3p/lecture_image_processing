# �ۑ�5���|�[�g

https://www.pakutaso.com/20140657168post-4246.html �̃C���X�g�����摜�Ƃ���D���̉摜�͏c900�摜�C��1600��f�ɂ�钷���`�̃f�B�W�^���J���[�摜�ł���D

ORG=imread('cat.jpg'); % ���摜�̓���  
ORG = rgb2gray(ORG); colormap(gray); colorbar;  
imagesc(ORG); axis image; % �摜�̕\��

�ɂ���āC���摜���O���[�X�P�[���ǂݍ��݁C�\���������ʂ�}�P�Ɏ����D

![���摜](https://github.com/luna3p/lecture_image_processing/blob/master/image/image5_1.PNG?raw=true)  
�}1 ���摜

���摜�̔��ʕ��͖@��p���ē�A�����s��. ���ʕ��͖@�Ƃ͑Ώە��̔Z�x�Ɣw�i�̔Z�x�Ƃ����ꂼ��ł��悭�܂Ƃ܂�, ����
�Ώە��Ɣw�i�̈Ⴂ����ʂł���悤��臒l�����߂���@�ł���. �܂��S��f�̔Z�x�̕��ϒl�����߂�. ���ɔZ�xt�ŃN���X�𕪂�, ���̂Q��
�N���X�̕��U, ���ϒl, ��f�������߂�. �N���X�����U�ƃN���X�ԕ��U�����߂�.�N���X�ԕ��U�̓����N���X�����U�̓��Ŋ���, ���̒l���ő�ƂȂ�悤�ȔZ�xt�����߂�. 


C1 = H(1:i); %�q�X�g�O������2�̃N���X�ɕ�����  
C2 = H(i+1:256);  
n1 = sum(C1); %��f���̎Z�o  
n2 = sum(C2);  
myu1 = mean(C1); %���ϒl�̎Z�o  
myu2 = mean(C2);  
sigma1 = var(C1); %���U�̎Z�o  
sigma2 = var(C2);  
sigma_w = (n1 *sigma1+n2*sigma2)/(n1+n2); %�N���X�����U�̎Z�o  
sigma_B = (n1 *(myu1-myu_T)^2+n2*(myu2-myu_T)^2)/(n1+n2); %�N���X�ԕ��U�̎Z�o  
if max_val<sigma_B/sigma_w  
max_val = sigma_B/sigma_w;  
max_thres =i;  


![���摜](https://github.com/luna3p/lecture_image_processing/blob/master/image/image5_2.PNG?raw=true)  
�}2 ���ʕ��͖@�ɂ���A���摜


���̓�l�摜��臒l�̒l��

disp(max_thres);

�ɂ���ĎQ�Ƃł�, 臒l�͂X�W�ƂȂ���. 