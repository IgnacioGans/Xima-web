# Xima-web


//Reduce Size Video
ffmpeg -i input.mp4 -vcodec h264 -acodec mp2 output.mp4
ffmpeg -i rk_XimaHotels.mp4 -vcodec h264 -acodec mp2 rk_XimaHotels_reduceSize.mp4 

// Remove Audio from Video
ffmpeg -i rk_XimaHotels.mp4 -c copy -an rk_XimaHotels-nosound.mp4
// Another sample to Remove Audio from video
ffmpeg -i rk_XimaHotels.mp4 -an -vcodec copy rk_XimaHotels-nosound.mp4
