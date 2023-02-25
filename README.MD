### ENCODE
This `encode` script is useful to converto from .mkv file to .mp4 or reduce bigest files.

# MAC OS INSTALLATION
```
brew install ffmpeg
```

# LINUX DEBIAN LIKE INSTALLATION
```
sudo apt update
sudo apt install ffmpeg
```

# WINDOWS 10+ INSTALLATION
Follow this link for Windows installation: 
[Windows ffmpeg setup](https://www.geeksforgeeks.org/how-to-install-ffmpeg-on-windows/)


# CHECKING FFMPEG INSTALLATION
You can check if ffmpeg installation was succesful by using the following command in your terminal:
```
ffmpeg -version
```

# PREPARING ENCODE SCRIPT
Create a simple file called `encode` (without extension) and put following code:
```bash
#!/usr/bin/env bash

ffmpeg -i "$1" -vcodec h264 -acodec aac "$2"
```

After that, apply the following execution permission:
```
chmod u+x encode
```

## USAGE
The next steps will show you how to use.

# FROM .MKV TO .MP4 USAGE
```
./encode input.mkv output.mp4
```

# REDUCE FILE SIZE USAGE
```
./encode input.mp4 output.mp4
```