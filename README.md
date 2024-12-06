# Commercial Cleaner 

CommercialCleaner is a command line utility to remove commercials from a video file at EDL file cutpoints. The EDL file is commonly created by the application ComSkip. It has executables that will run under Windows x64, OSX x64, Linux x64 and Linux ARM. 

The application transitions very smoothly in to and out from where the commercials were. It can also optionally: 

- Remove an amount of time in seconds at the start of the video (in case the recording starts before the show begins) 
- Remove an amount of time in seconds at the end of the video (in case the recording runs after the show ends) 
- Allow you to set the video codec you desire for the output file 
- Allow you to set the audio codec you desire for the output file 
- List available audio and video codecs (for the 2 commands above) 

## Parameters (case insensitive): 

- -ffmpegpPath=Path to the ffmpeg executable.  Just the folder, the exe is assumed to be ffmpeg.exe or ffmpeg.
- -inFile=The full path of the input video file that will be cleaned. 
- Optional: -startTimeRemoveSeconds=Amount of time, in seconds, to remove from the beginning of the video. Default: 0 
- Optional: -endTimeRemoveSeconds=Amount of time, in seconds, to remove from the end of the video. Default: 0 
- Optional: -listCodecs=List all available video and audio codecs. 
- Optional: -videoCodec=Video codec to use for the outputFile. The codec name is case sensitive. Default: Same as the input file. 
- Optional: -audioCodec=Audio codec to use for the outputFile. The codec name is case sensitive. Default: Same as the input file. 

The cleaned video file will be in the same directory as the original file, named the same as the original with “\_clean” appended.  The created file container will always be MKV, regardless of the input format. 

For example, the following command will clean the specified video file and save its output to   C:\\My Movies\\My Little Pony\_clean.mkv 
```
CommercialCleaner -mpegPath="C:\mpeg\bin” -inFile="c:\\My Movies\\My Little Pony.ts" -videoCodec=libx265 
```

## Note
CommercialCleaner is CharityWare. If you like this program and find it of value, please consider making a donation to a local charity that benefits children such as Special Olympics. 
