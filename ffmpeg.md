1. Convert all image
```
FOR /F "tokens=*" %G IN ('dir /b *.flac') DO ffmpeg -i "%G" -acodec mp3 "%~nG.mp3"
```

2. Rename all item

```
FOR /F "tokens=*" %G IN ('dir /b *.flac') DO ffmpeg -i "%G" -acodec mp3 "%~nG.mp3"
```


3. Cut vieo

```
ffmpeg -ss 00:01:00 -to 00:02:00 -i input.mp4 -c copy output.mp4
```

4. Extract audio

https://www.baeldung.com/linux/ffmpeg-audio-from-video
https://stackoverflow.com/questions/9913032/how-can-i-extract-audio-from-video-with-ffmpeg

```
ffmpeg -i input.mkv -vn -acodec copy output.aac
ffmpeg -i input.mkv -map 0:a -acodec copy output.aac
```
