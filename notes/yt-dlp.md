# yt-dlp

## Installation
Install on Mac:
```bash
brew install yt-dlp
```

## Help
```bash
man yt-dlp
```

## Check video's available formats
```bash
yt-dlp -F [video-url]
```

## Download
```bash
yt-dlp [video-url]
yt-dlp [video-url] -f "bestvideo[height<=1080][ext=mp4]+bestaudio[ext=m4a]/best[ext=mp4]/best"
```