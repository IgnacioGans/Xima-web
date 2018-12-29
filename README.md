[Rich Text Tools](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

# Xima-web

## Simple Convert

ffmpeg -i input.mkv output.mp4
ffmpeg -i Converter_Xima_Videos\Xima.mp4 Converter_Xima_Videos\Xima.ogg


## Reduce Size Video

ffmpeg -i input.mp4 -vcodec h264 -acodec mp2 output.mp4
ffmpeg -i Xima.mp4 -vcodec h264 -acodec aac Converter_Xima_Videos\Xima.mp4
ffmpeg -i rk_XimaHotels.mp4 -vcodec h264 -acodec mp2 rk_XimaHotels_reduceSize.mp4 

## Remove Audio from Video
ffmpeg -i rk_XimaHotels.mp4 -c copy -an rk_XimaHotels-nosound.mp4

## Another sample to Remove Audio from video
#ffmpeg -i rk_XimaHotels.mp4 -an -vcodec copy rk_XimaHotels-nosound.mp4

## Convert MP4 to WebM
ffmpeg -i Converter_Xima_Videos\Xima.mp4 -c:v libvpx -crf 10 -b:v 1M -c:a libvorbis Converter_Xima_Videos\Xima.webm

## Convert MP4 to Ogg/Ogv

ffmpeg -i Converter_Xima_Videos\Xima.mp4 -codec:v libtheora -qscale:v 6 -codec:a libvorbis -qscale:a 6 Converter_Xima_Videos\Xima.ogg

## Re-cut Fragment of video
ffmpeg -i video.mp4 -ss 35 -t 30 fragmento.mp4
ffmpeg -i video.mp4 -ss 00:35 -to 01:05 fragmento.mp4

ffmpeg -i Xima_Cusco_low2500kb.mp4 -ss 00:00 -to 00:30 Xima_Cusco_low_30seg.mp4
ffmpeg -i Xima_Puno_low2500kb.mp4 -ss 00:00 -to 00:30 Xima_Puno_low_30seg.mp4

# PowerShell Windows Prompt

 get-childitem | ForEach-Object { Move-Item -LiteralPath $_.name $_.name.Replace("(1)","")}
