��򵥵Ļ���FFmpeg����Ƶ������ 2
Simplest FFmpeg Player 2

������ Lei Xiaohua
leixiaohua1020@126.com
�й���ý��ѧ/���ֵ��Ӽ���
Communication University of China / Digital TV Technology
http://blog.csdn.net/leixiaohua1020


������ʵ������Ƶ�ļ��Ľ������ʾ��֧��HEVC��H.264��MPEG2�ȣ���
����򵥵�FFmpeg��Ƶ���뷽��Ľ̡̳�
ͨ��ѧϰ�����ӿ����˽�FFmpeg�Ľ������̡�
��Ŀ�����������̣�
simplest_ffmpeg_player����׼�棬FFmpegѧϰ�Ŀ�ʼ��
simplest_ffmpeg_player_su��SU��SDL Update���棬�����˼򵥵�SDL��Event��

��ע:
��׼���ڲ�����Ƶ��ʱ�򣬻�����ʾʹ����ʱ40ms�ķ�ʽ����ô�������������
��1��SDL�����Ĵ����޷��ƶ���һֱ��ʾ��æµ״̬
��2��������ʾ�������ϸ��40msһ֡����Ϊ��û�п��ǽ����ʱ�䡣
SU��SDL Update��������Ƶ����Ĺ����У�����ʹ����ʱ40ms�ķ�ʽ�����Ǵ�����
һ���̣߳�ÿ��40ms����һ���Զ������Ϣ����֪���������н�����ʾ��������֮��
��1��SDL�����Ĵ��ڿ����ƶ���
��2��������ʾ���ϸ��40msһ֡


This software is a simplest video player based on FFmpeg.
Suitable for beginner of FFmpeg.
Solutions contains 2 Project:
simplest_ffmpeg_player��Standard Version, suitable for biginner.
simplest_ffmpeg_player_su��SU��SDL Update��Version, Add SDL Event.

Remark:
Standard Version use's SDL_Delay() to control video's frame rate, it has 2
disadvantages:
(1)SDL's Screen can't be moved and always "Busy".
(2)Frame rate can't be accurate because it doesn't consider the time consumed 
by avcodec_decode_video2()
SU��SDL Update��Version solved 2 problems above. It create a thread to send SDL 
Event every 40ms to tell the main loop to decode and show video frames.
