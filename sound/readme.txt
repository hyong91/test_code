WAV Parser�Ƕ�WAV�ļ��ķ����ͷ�װ������ֻ���Standard WAV File��

SND Common��Playback ��Record��ͬ��������SetParams��ReadPCM��WritePCM�ȣ�

Playback��Record�ͷֱ��ǲ���¼���������ˡ�

����ʱ��Ҫ����libasound  ��-lasound)
gcc -o lplay lplay.c wav_parser.c sndwav_common.c -lasound
gcc -o lrecord lrecord.c wav_parser.c sndwav_common.c -lasound

��������alsa�����������豸�����øó�������õ�OSM�������С�
alsa����û������������������alsamixer��������������alsaconf��������һ��������