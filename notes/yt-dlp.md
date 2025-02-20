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
URL="https://www.youtube.com/watch?v=eit0HS3UDzo"; yt-dlp "$URL" -f "bestvideo[height<=1080][ext=mp4]+bestaudio[ext=m4a]/best[ext=mp4]/best"

# mass download videos (file list.txt contains list of links)
a=1; total=$(wc -l list.txt | awk '// { print $1}'); \
for i in $(cat list.txt); do \
echo "Download ${a}/${total}"; a=$((a+1)); \
yt-dlp ${i} -f "bestvideo[height<=1080][ext=mp4]+bestaudio[ext=m4a]/best[ext=mp4]/best"; \ 
done
```
