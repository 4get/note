
linux-2.6.34/Documentation/sound/alsa/Procfile.txt

echo 5 > /proc/asound/card0/pcm0p/xrun_debug
cat /proc/asound/card*/pcm*p/sub*/status | grep tstamp

-调音量

	amixer set Master 100 unmute

-播放噪音，吱吱吱

    aplay  -f dat /dev/mem
