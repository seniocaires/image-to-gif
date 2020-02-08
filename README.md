# Image to gif

```

docker build -t seniocaires/imagemagick .

docker run -it --rm -v $(pwd):/images -w images seniocaires/imagemagick

convert -delay 50 -loop 0 -background none -debug all  *.jpg  animated.gif

ffmpeg -framerate 2 -pattern_type glob -i '*.jpg' -c:v libx264 -r 30 -pix_fmt yuv420p video.mp4

```
