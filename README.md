# YouTube Downloader CLI Tool

* A command-line application for downloading YouTube videos and the qulity is maximum available quality. This project is intended for educational purposes and demonstrates how to use Go, concurrency, and external commands for media processing.

## Features
- **Download YouTube Videos**: Extracts video and audio streams separately.
- **Merge Video and Audio**: Combines video and audio streams into a single file.
- **Animated Spinner and Elapsed Time**: Provides real-time feedback with an animated spinner for downloading and elapsed time display for merging.
- **Customizable Save Location**: Allows specifying the output directory for saved files.

## Prerequisites
- **Go 1.16+**: The project is built with Go. [Download Go here](https://golang.org/dl/).
- **Python, Pyinstaller and Nuitka (optional)**: If you want to compile the `merge_media.py` script into an executable, Python and Nuitka are needed.

## Project Structure
yt-Downloader
├── %SystemDrive%/                # Temporary directory (created by Nuitka or other build processes)
├── merge_media.build/             # Temporary build folder created by Nuitka
├── merge_media.dist/              # Distribution folder with the Nuitka compiled executable and dependencies
├── merge_media.onefile-build/     # Additional build directory for Nuitka
├── yt-service/                    # Core service files and subdirectories
│   ├── audio/                     # Directory for storing audio files
│   │   └── audio.fo               # Sample or placeholder audio file
│   ├── video/                     # Directory for storing video files
│   │   └── video.go               # Sample or placeholder video file
│   ├── python/                    # Python scripts folder
│   │   └── merge_media.py         # Python script for merging video and audio
│   ├── helpers/                   # Helper functions for the project
│   │   └── helpers.go             # Go file with utility/helper functions
│   └── temp/                      # Temporary folder, possibly for processing or intermediate files
├── go.mod                         # Go module file for managing dependencies
├── go.sum                         # Go module checksum file
├── main.go                        # Main application entry point
├── merge_media.exe                # Compiled executable of merge_media.py (created by Nuitka)
├── README.md                      # Project documentation
└── YouTube-Downloader.exe         # Compiled Go application executable


## Setup
1. Clone the repository:

 ```bash
       git clone https://github.com/ShebinSp/yt-downloader.git
       cd yt-downloader
```
2. Install Go dependencies (if any). This project requires no external Go dependencies outside the standard library.

3. (Optional) Compile merge_media.py using Nuitka:
    ```nuitka --standalone --output-dir=merge_media.dist merge_media.py```

### Usage
* Run the application from the command line:

```bash
    Copy code
    go run main.go
    Enter the YouTube video URL.
    The application will start downloading the video and audio streams.
    After downloading, it will merge the video and audio and save it to the /Download folder.
```
### Disclaimer
**This tool is intended solely for personal and educational use. Ensure compliance with YouTube's terms of service and respect content creators' rights.**


