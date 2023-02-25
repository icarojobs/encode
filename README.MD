### ENCODE
This `encode` script is useful to converto from .mkv file to .mp4 or reduce bigest files.

# INSTALLATION (MAC OS)
```
brew install ffmpeg
```

# PREPARING ENCODE SCRIPT
Create a simple file called `encode` with the following code:
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