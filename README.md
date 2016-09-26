# ModifiedKxMovie

It is a backup of KxMovie that used in Eleven RTSP streaming player

## FFMPEG:
### Version & Modification:

1. FFMPEG version is 2.7.2
2. "rtpdec.h" and "rtpdec.c" are modified to fulfill the needs of sending "RR" every 10~20 seconds.
   As N3292x cutting off the connection after no incoming RTCP packets in 20 seconds, the audio would be muted without this modification.

### Installation:

1. Follow instructions in https://github.com/kewlbear/FFmpeg-iOS-build-script
2. Editing build-ffmpeg.sh can change targeting FFMPEG version.

## Installation of KxMovie:
### Steps:
1. Copy FFmpeg-iOS & kxmovie folder into project
2. Add header path in "Build Settings"
3. Add library in "Build Phases"
4. It should be done

### Usages:
1. Follow instructions in https://github.com/kolyvan/kxmovie
2. Modify latency in KxMovieDecoder.m
3. kxmovie-Prefix.pch needs to be added in "Prefixed  Header", or the error "UIImage not found" or etc. will pop out.
