# FFMPEG
1. [ffprobe](#ffprobe)
2. [ffmpeg](#ffmpeg)

## ffprobe
```bash
ffprobe -show_format video.mp4
ffprobe -show_error video.mp4
ffprobe -show_streams video.mp4
```

## ffmpeg

Downloading:
```bash
ffmpeg -i HLS_MANIFSET_URL -c copy -bsf:a aac_adtstoasc output.mp4
```

Streaming:
```bash

# Send FLV stream over RTMP to VK
url=rtmp://ovsu.okcdn.ru/input;key=1234_5678_asdf;\
ffmpeg -stream_loop 1 -re -i video.mp4 -c copy -f flv ${url}/${key}
```
