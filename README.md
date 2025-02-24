Hello! 

This repository has 3 python scripts. 

***First python script is file_mover.py***, asks end-user to select source and destination folders. It then moves all files from the selected source folder and its subfolders to the chosen destination folder.


***Second python script is renaming_files.py***, provides functionality to rename files within a selected folder. It includes two options for renaming:

Rename by Creation Datetime: Renames files based on their creation datetime. Files are renamed using a format of "YYYYMMDD_HHMMSS" followed by the original file extension. If multiple files have the same creation datetime, a counter is added to the filename to avoid duplicates.

Rename by Date Taken from Metadata: Attempts to extract the date taken from image files' metadata. If successful, it renames the files using the extracted date and time in the format "YYYYMMDD_HHMMSS" followed by the original file extension. If metadata extraction fails or if the file is not an image, it falls back to renaming by creation datetime.

***Third python script is photo_sorter_by_name_or_by_datetaken.py***, this script organizes photos in a selected folder by either their filenames or the dates they were taken, with the option chosen by the user at runtime.

Features:
***Organize by Filename:*** Assumes filenames follow the format YYYYMMDD_xxx.ext. It extracts the year and month from the filename, creates corresponding folders, and moves the photos into these folders.

***Organize by Date Taken:*** Uses EXIF metadata to determine the date the photo was taken. It extracts the year and month from the EXIF data, creates corresponding folders, and moves the photos into these folders.

***Handle Duplicate Names:*** If a file with the same name already exists in the destination folder, it appends a unique suffix to the filename to avoid overwriting.



***NOTE:***

***The script can technically handle any file type for renaming by creation date, but metadata-based renaming (using the date taken) is specifically effective for JPEG files.***

***Which means that the second and third scripts will not function properly if the file lacks a Date Taken value, as those two scripts rely on extracting EXIF data to rename (second script) and move (third script) the files. EXIF (Exchangeable Image File Format) data is a type of metadata embedded within image files, primarily JPEG and TIFF formats. Additionally, the second and third scripts will not work properly with HEIF files.***

***Easy way to run***

I've converted these scripts into executable (EXE) files for your convenience. Simply run the EXE files and follow the instructions. Unfortunately, I couldn't upload them to GitHub due to the 25MB limit, as the EXE files are around 50-60MB. You can download the files from the following link: [https://drive.google.com/drive/folders/1FDDpCKrTq-wWm9KTNNYeifsRooe7gJ83?usp=sharing](https://drive.google.com/drive/u/9/folders/1vHxWnsvPEbYWIjmbyeCbiD6OL4F8Bnav). 


***Harder way to to RUN*** LOL


To run the provided Python scripts, you can follow these general steps:

***1. Install Python:***
If you haven't installed Python on your system, you can download and install it from the official Python website: https://www.python.org/downloads/.

***2. Create Backup:***
Before running any scripts that modify or move files, it's a good practice to create a backup of the relevant folders to avoid accidental data loss.

***3. Run Scripts:***
Open a command prompt in the folder that contains the scripts that you want to run, like this: 

<img width="626" alt="1" src="https://github.com/radenko98/Photo-Move-Rename-Sort/assets/22021972/cfb66369-3256-4baf-8eea-30bf9390da64">


***4.Path*** - 
Delete the path in the file explorer and type CMD

<img width="564" alt="2" src="https://github.com/radenko98/Photo-Move-Rename-Sort/assets/22021972/b05cefb8-e11a-4ff3-8c37-c179f0e67b4c">


***5. Running the script*** - Type the command "python file_mover.py" and press enter

<img width="712" alt="3" src="https://github.com/radenko98/Photo-Move-Rename-Sort/assets/22021972/9a4373da-f7a8-4f4b-849b-89edb3103f22">






Alternatively, if you are using Python 3, replace python with python3 in the commands
Check the output of each script in the console to ensure there are no errors and to see the progress or any messages printed by the scripts.




***More information on how the scripts work***

***File_mover.py script will ask you to select source and destination folder like this.***

Select source folder:

<img width="761" alt="4" src="https://github.com/radenko98/Photo-Move-Rename-Sort/assets/22021972/d27577a3-af88-477f-b8e8-f5597075a953">


Select the destination folder:

<img width="729" alt="5" src="https://github.com/radenko98/Photo-Move-Rename-Sort/assets/22021972/a789e7f2-e689-4ccc-bba6-4f2b5fea4498">



***Renaming_files.py script will ask you to select the folder that contains the files you want renamed.***
After you select the folder, you will be asked to choose between renaming folder according to their Creation Datetime or their Date Taken value from Metadata. If you are renaming photos and videos, choose renaming files according to Date Taken value from Metadata. Like this:

<img width="260" alt="7" src="https://github.com/radenko98/Photo-Move-Rename-Sort/assets/22021972/983b15db-44e2-48ff-8051-fff7fcf77fd4">


***The "Photo_sorter.py" script prompts users to select a folder containing files to be organized according to their date taken value (as recorded in metadata) or according to filename.***

<img width="821" alt="6" src="https://github.com/radenko98/Photo-Move-Rename-Sort/assets/22021972/49d7ddd7-ec00-49dc-9fb5-a53182d51cce">



***In the end you will get a folder like this:***


![Example](https://github.com/radenko98/Photo-Move-Rename-Sort/assets/22021972/d6eeb744-0c3b-4478-998f-fa09211d8f43)





