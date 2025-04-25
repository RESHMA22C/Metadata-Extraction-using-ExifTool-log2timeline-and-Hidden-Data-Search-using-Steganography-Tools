# Metadata-Extraction-using-ExifTool-log2timeline-and-Hidden-Data-Search-using-Steganography-Tools
# NAME: Reshma C
# REG NO: 212223040168
## AIM:
To extract metadata, perform timeline analysis, and search for hidden data using forensic tools like ExifTool, log2timeline, and steganography detection tools.

## DESIGN STEPS:
### Step 1:
Use exiftool to extract metadata from files such as images, documents, and videos.

### Step 2:
Use log2timeline and plaso to create and analyze event timelines from system logs and file metadata.

### Step 3:
Apply steganography detection tools like steghide, zsteg, or binwalk to uncover hidden data in media files.

## PROGRAM:
Metadata and Timeline Forensics, Steganography Analysis Steps
## OUTPUT:
# A. Using ExifTool – for file metadata
Install:
~~~
sudo apt update
sudo apt install exiftool -y
~~~
### Extract metadata from a file:
~~~
exiftool image.jpg
~~~
### Batch process a folder:
~~~
exiftool -r /path/to/folder
~~~
# Useful flags:
-G: Show metadata group

-time:all: Show only timestamps

-GPSLatitude -GPSLongitude: Extract GPS data
![image](https://github.com/user-attachments/assets/4774b7fa-5d36-4941-9afb-58bd1f74f03e)

# install log2timeline
~~~
sudo apt install plaso -y
sudo apt install steghide -y
~~~
# Embed data
~~~
steghide embed -cf /home/kali/Downloads/wallpaper.jpg -ef /home/kali/Downloads/secret.txt
~~~
![image](https://github.com/user-attachments/assets/daf5fb5d-bc00-4a30-90b6-4277a4a3ea50)
# Extract hidden data:
~~~
steghide extract -sf hidden.jpg
~~~
![image](https://github.com/user-attachments/assets/9abbc979-fe73-4c54-8d0e-908c0bcc7c37)
# Using binwalk – for file analysis
~~~
sudo apt install binwalk -y
binwalk suspicious.jpg
~~~
![image](https://github.com/user-attachments/assets/51409417-97e1-4db5-9731-0c1e17b74902)

## RESULT:
Metadata was successfully extracted, timeline analysis was completed, and hidden data was identified using steganography tools.

