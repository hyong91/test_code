WAV Parser是对WAV文件的分析和封装，这里只针对Standard WAV File；

SND Common是Playback 和Record共同操作，如SetParams、ReadPCM和WritePCM等；

Playback和Record就分别是播放录音的主体了。

编译时需要链接libasound  （-lasound)
gcc -o lplay lplay.c wav_parser.c sndwav_common.c -lasound
gcc -o lrecord lrecord.c wav_parser.c sndwav_common.c -lasound

必须是用alsa驱动的声卡设备才能用该程序，如果用的OSM驱动则不行。
alsa驱动没有声音可以输入命令alsamixer调节音量，或者alsaconf重新配置一下声卡。