��򵥵Ļ���FFmpeg����Ƶ������ 2
Simplest FFmpeg Player 2

�ҵ�ѧϰ����


������ʵ������Ƶ�ļ��Ľ������ʾ��֧��HEVC��H.264��MPEG2�ȣ���
����򵥵�FFmpeg��Ƶ���뷽��Ľ̡̳�
ͨ��ѧϰ�����ӿ����˽�FFmpeg�Ľ������̡�
��Ŀ����6�����̣�
simplest_ffmpeg_player����׼�棬FFmpegѧϰ�Ŀ�ʼ��
simplest_ffmpeg_player_su��SU��SDL Update���棬�����˼򵥵�SDL��Event��
simplest_ffmpeg_decoder��һ�������˷�װ��ʽ�����ܵĽ�������ʹ����libavcodec��libavformat��
simplest_ffmpeg_decoder_pure��һ�������Ľ�������ֻʹ��libavcodec��û��ʹ��libavformat����
simplest_video_play_sdl2��ʹ��SDL2����YUV�����ӡ�
simplest_ffmpeg_helloworld�����FFmpeg������Ϣ��

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
Solutions contains 6 Project:
simplest_ffmpeg_player: Standard Version, suitable for biginner.
simplest_ffmpeg_player_su: SU��SDL Update��Version, Add SDL Event.
simplest_ffmpeg_decoder_pure: A pure decoder. Only use libavcodec (Without libavformat).
simplest_ffmpeg_decoder: A decoder that can demux container format. Uses libavcodec and libavformat.
simplest_video_play_sdl2: Example about using SDL2 play YUV data.
simplest_ffmpeg_helloworld: Output informations about FFmpeg libraries.

Remark:
Standard Version use's SDL_Delay() to control video's frame rate, it has 2
disadvantages:
(1)SDL's Screen can't be moved and always "Busy".
(2)Frame rate can't be accurate because it doesn't consider the time consumed 
by avcodec_decode_video2()
SU��SDL Update��Version solved 2 problems above. It create a thread to send SDL 
Event every 40ms to tell the main loop to decode and show video frames.
