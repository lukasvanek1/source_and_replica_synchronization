Code based on the following conditions:
Test Task

Please implement a program that synchronizes two folders: source and replica. The program should maintain a full, identical copy of source folder at replica folder. 
# completed

Solve the test task by writing a program in one of these programming languages: 
# python

Synchronization must be one-way: after the synchronization content of the replica folder should be modified to exactly match content of the source folder; 
# done and tested in VS code on a Windows laptop

Synchronization should be performed periodically; 
# done, 30 seconds, the interval time in seconds can be adjusted in the command line

File creation/copying/removal operations should be logged to a file and to the console output; 
# done - the file path is a part of the command line. Shall there be none created by the user, the program creates one at the time of the first execution. Copy of the most recent log content as bellow

Folder paths, synchronization interval and log file path should be provided using the command line arguments; 
# the actual command line used for testing on my laptop (and recorded in the log): 
python sync_code.py "C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source" "C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica" 30 "C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync.log"
# where: python sync_code.py "source folder path" "replica folder path" number of seconds for the execution interval "log file path"

It is undesirable to use third-party libraries that implement folder synchronization; 
# only python standard libraries used

It is allowed (and recommended) to use external libraries implementing other well-known algorithms. For example, there is no point in implementing yet another function that calculates MD5 if you need it for the task – it is perfectly acceptable to use a third-party (or built-in) library; 
# used several built-in python libraries - all stated in the imports at the top of the script. Used SHA-256 instead of MD5 for higher encryption, but MD5 can be used in case of dealing with large files causing the processing time with SHA-256 being too long

The solution should be presented in the form of a link to the public GitHub repository. 
# https://github.com/lukasvanek1/source_and_replica_synchronization.git

# Copy of the the most recent log (some previous versions were deleted while testing):
2024-10-05 05:12:19 - Starting synchronization from C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source to C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica every 30 seconds
2024-10-05 05:12:19 - Source folder contains 7 files and 0 directories.
2024-10-05 05:12:19 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:12:19 - Total operations to perform: 13
2024-10-05 05:16:51 - Starting synchronization from C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source to C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica every 30 seconds
2024-10-05 05:16:51 - Source folder contains 7 files and 0 directories.
2024-10-05 05:16:51 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:16:51 - Total operations to perform: 13
2024-10-05 05:16:51 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New doc 4.docx
2024-10-05 05:16:51 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New doc 4.docx
2024-10-05 05:16:51 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New doc 5.docx
2024-10-05 05:16:51 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New doc 5.docx
2024-10-05 05:16:51 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\T3-21-2 Announcements.xlsx
2024-10-05 05:16:51 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\.\T3-21-2 Announcements.xlsx
2024-10-05 05:16:51 - Synchronization complete. Time taken: 0.03 seconds
2024-10-05 05:17:21 - Source folder contains 7 files and 0 directories.
2024-10-05 05:17:21 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:17:21 - Total operations to perform: 13
2024-10-05 05:17:21 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New doc 4.docx
2024-10-05 05:17:21 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New doc 4.docx
2024-10-05 05:17:21 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New doc 5.docx
2024-10-05 05:17:21 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New doc 5.docx
2024-10-05 05:17:21 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\T3-21-2 Announcements.xlsx
2024-10-05 05:17:21 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\.\T3-21-2 Announcements.xlsx
2024-10-05 05:17:21 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 05:17:51 - Source folder contains 7 files and 0 directories.
2024-10-05 05:17:51 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:17:51 - Total operations to perform: 13
2024-10-05 05:17:51 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New doc 4.docx
2024-10-05 05:17:51 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New doc 4.docx
2024-10-05 05:17:51 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New doc 5.docx
2024-10-05 05:17:51 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New doc 5.docx
2024-10-05 05:17:51 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\T3-21-2 Announcements.xlsx
2024-10-05 05:17:51 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\.\T3-21-2 Announcements.xlsx
2024-10-05 05:17:51 - Synchronization complete. Time taken: 0.02 seconds
2024-10-05 05:18:21 - Source folder contains 7 files and 0 directories.
2024-10-05 05:18:21 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:18:21 - Total operations to perform: 13
2024-10-05 05:18:21 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New doc 4.docx
2024-10-05 05:18:21 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New doc 4.docx
2024-10-05 05:18:21 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New doc 5.docx
2024-10-05 05:18:21 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New doc 5.docx
2024-10-05 05:18:21 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\T3-21-2 Announcements.xlsx
2024-10-05 05:18:21 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\.\T3-21-2 Announcements.xlsx
2024-10-05 05:18:21 - Synchronization complete. Time taken: 0.02 seconds
2024-10-05 05:18:51 - Source folder contains 7 files and 0 directories.
2024-10-05 05:18:51 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:18:51 - Total operations to perform: 13
2024-10-05 05:18:51 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New doc 4.docx
2024-10-05 05:18:51 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New doc 4.docx
2024-10-05 05:18:51 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New doc 5.docx
2024-10-05 05:18:51 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New doc 5.docx
2024-10-05 05:18:51 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\T3-21-2 Announcements.xlsx
2024-10-05 05:18:51 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\.\T3-21-2 Announcements.xlsx
2024-10-05 05:18:51 - Synchronization complete. Time taken: 0.02 seconds
2024-10-05 05:19:21 - Source folder contains 7 files and 0 directories.
2024-10-05 05:19:21 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:19:21 - Total operations to perform: 13
2024-10-05 05:19:21 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New doc 4.docx
2024-10-05 05:19:21 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New doc 4.docx
2024-10-05 05:19:21 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New doc 5.docx
2024-10-05 05:19:21 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New doc 5.docx
2024-10-05 05:19:21 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\T3-21-2 Announcements.xlsx
2024-10-05 05:19:21 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\.\T3-21-2 Announcements.xlsx
2024-10-05 05:19:21 - Synchronization complete. Time taken: 0.02 seconds
2024-10-05 05:19:51 - Source folder contains 7 files and 0 directories.
2024-10-05 05:19:51 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:19:51 - Total operations to perform: 13
2024-10-05 05:19:51 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New doc 4.docx
2024-10-05 05:19:51 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New doc 4.docx
2024-10-05 05:19:51 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New doc 5.docx
2024-10-05 05:19:51 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New doc 5.docx
2024-10-05 05:19:51 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\T3-21-2 Announcements.xlsx
2024-10-05 05:19:51 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\.\T3-21-2 Announcements.xlsx
2024-10-05 05:19:51 - Synchronization complete. Time taken: 0.02 seconds
2024-10-05 05:20:21 - Source folder contains 7 files and 0 directories.
2024-10-05 05:20:21 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:20:21 - Total operations to perform: 13
2024-10-05 05:20:21 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New doc 4.docx
2024-10-05 05:20:21 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New doc 4.docx
2024-10-05 05:20:21 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New doc 5.docx
2024-10-05 05:20:21 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New doc 5.docx
2024-10-05 05:20:21 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\T3-21-2 Announcements.xlsx
2024-10-05 05:20:21 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\.\T3-21-2 Announcements.xlsx
2024-10-05 05:20:21 - Synchronization complete. Time taken: 0.02 seconds
2024-10-05 05:20:51 - Source folder contains 8 files and 0 directories.
2024-10-05 05:20:51 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:20:51 - Total operations to perform: 14
2024-10-05 05:20:51 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New doc 4.docx
2024-10-05 05:20:51 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New doc 4.docx
2024-10-05 05:20:51 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New doc 5.docx
2024-10-05 05:20:51 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New doc 5.docx
2024-10-05 05:20:51 - Synchronization complete. Time taken: 0.02 seconds
2024-10-05 05:21:21 - Source folder contains 8 files and 0 directories.
2024-10-05 05:21:21 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:21:21 - Total operations to perform: 14
2024-10-05 05:21:21 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New doc 4.docx
2024-10-05 05:21:21 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New doc 4.docx
2024-10-05 05:21:21 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New doc 5.docx
2024-10-05 05:21:21 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New doc 5.docx
2024-10-05 05:21:21 - Synchronization complete. Time taken: 0.02 seconds
2024-10-05 05:21:51 - Source folder contains 6 files and 0 directories.
2024-10-05 05:21:51 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:21:51 - Total operations to perform: 12
2024-10-05 05:21:51 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 05:22:21 - Source folder contains 7 files and 0 directories.
2024-10-05 05:22:21 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:22:21 - Total operations to perform: 13
2024-10-05 05:22:21 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\File4.odt
2024-10-05 05:22:21 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\File4.odt
2024-10-05 05:22:21 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 05:22:51 - Source folder contains 7 files and 0 directories.
2024-10-05 05:22:51 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:22:51 - Total operations to perform: 13
2024-10-05 05:22:51 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\File4.odt
2024-10-05 05:22:51 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\File4.odt
2024-10-05 05:22:51 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 05:23:21 - Source folder contains 6 files and 0 directories.
2024-10-05 05:23:21 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:23:21 - Total operations to perform: 12
2024-10-05 05:23:21 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 05:23:51 - Source folder contains 6 files and 0 directories.
2024-10-05 05:23:51 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:23:51 - Total operations to perform: 12
2024-10-05 05:23:51 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 05:24:21 - Source folder contains 6 files and 0 directories.
2024-10-05 05:24:21 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:24:21 - Total operations to perform: 12
2024-10-05 05:24:21 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 05:24:51 - Source folder contains 6 files and 0 directories.
2024-10-05 05:24:51 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:24:51 - Total operations to perform: 12
2024-10-05 05:24:51 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 05:25:21 - Source folder contains 6 files and 0 directories.
2024-10-05 05:25:21 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:25:21 - Total operations to perform: 12
2024-10-05 05:25:21 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 05:25:51 - Source folder contains 6 files and 0 directories.
2024-10-05 05:25:51 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:25:51 - Total operations to perform: 12
2024-10-05 05:25:51 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 05:26:21 - Source folder contains 6 files and 0 directories.
2024-10-05 05:26:21 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:26:21 - Total operations to perform: 12
2024-10-05 05:26:21 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 05:26:51 - Source folder contains 6 files and 0 directories.
2024-10-05 05:26:51 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:26:51 - Total operations to perform: 12
2024-10-05 05:26:51 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 05:27:21 - Source folder contains 6 files and 0 directories.
2024-10-05 05:27:21 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:27:21 - Total operations to perform: 12
2024-10-05 05:27:21 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 05:27:51 - Source folder contains 6 files and 0 directories.
2024-10-05 05:27:51 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:27:51 - Total operations to perform: 12
2024-10-05 05:27:51 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 05:28:21 - Source folder contains 6 files and 0 directories.
2024-10-05 05:28:21 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:28:21 - Total operations to perform: 12
2024-10-05 05:28:21 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 05:28:51 - Source folder contains 6 files and 0 directories.
2024-10-05 05:28:51 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:28:51 - Total operations to perform: 12
2024-10-05 05:28:51 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 05:29:21 - Source folder contains 6 files and 0 directories.
2024-10-05 05:29:21 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:29:21 - Total operations to perform: 12
2024-10-05 05:29:21 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 05:29:51 - Source folder contains 6 files and 0 directories.
2024-10-05 05:29:51 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:29:51 - Total operations to perform: 12
2024-10-05 05:29:51 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 05:30:21 - Source folder contains 6 files and 0 directories.
2024-10-05 05:30:21 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:30:21 - Total operations to perform: 12
2024-10-05 05:30:21 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 05:30:51 - Source folder contains 6 files and 0 directories.
2024-10-05 05:30:51 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:30:51 - Total operations to perform: 12
2024-10-05 05:30:51 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 05:31:21 - Source folder contains 6 files and 0 directories.
2024-10-05 05:31:21 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:31:21 - Total operations to perform: 12
2024-10-05 05:31:21 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 05:31:51 - Source folder contains 6 files and 0 directories.
2024-10-05 05:31:51 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:31:51 - Total operations to perform: 12
2024-10-05 05:31:51 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 05:32:21 - Source folder contains 6 files and 0 directories.
2024-10-05 05:32:21 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:32:21 - Total operations to perform: 12
2024-10-05 05:32:21 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 05:32:51 - Source folder contains 6 files and 0 directories.
2024-10-05 05:32:51 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:32:51 - Total operations to perform: 12
2024-10-05 05:32:51 - Synchronization complete. Time taken: 0.02 seconds
2024-10-05 05:33:21 - Source folder contains 6 files and 0 directories.
2024-10-05 05:33:21 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:33:21 - Total operations to perform: 12
2024-10-05 05:33:21 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 05:33:51 - Source folder contains 6 files and 0 directories.
2024-10-05 05:33:51 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:33:51 - Total operations to perform: 12
2024-10-05 05:33:51 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 05:34:21 - Source folder contains 6 files and 0 directories.
2024-10-05 05:34:21 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:34:21 - Total operations to perform: 12
2024-10-05 05:34:21 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 05:34:51 - Source folder contains 6 files and 0 directories.
2024-10-05 05:34:51 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:34:51 - Total operations to perform: 12
2024-10-05 05:34:51 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 05:35:21 - Source folder contains 6 files and 0 directories.
2024-10-05 05:35:21 - Replica folder contains 6 files and 0 directories.
2024-10-05 05:35:21 - Total operations to perform: 12
2024-10-05 05:35:21 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 05:35:30 - Received interrupt signal. Exiting gracefully...
2024-10-05 06:46:49 - Starting synchronization from C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source to C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica every 30 seconds
2024-10-05 06:46:49 - Source folder contains 7 files and 0 directories.
2024-10-05 06:46:49 - Replica folder contains 7 files and 0 directories.
2024-10-05 06:46:49 - Total operations to perform: 14
2024-10-05 06:54:14 - Starting synchronization from C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source to C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica every 30 seconds
2024-10-05 06:54:14 - Source folder contains 7 files and 0 directories.
2024-10-05 06:54:14 - Replica folder contains 7 files and 0 directories.
2024-10-05 06:54:14 - Total operations to perform: 14
2024-10-05 06:55:49 - Starting synchronization from C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source to C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica every 30 seconds
2024-10-05 06:55:49 - Source folder contains 7 files and 0 directories.
2024-10-05 06:55:49 - Replica folder contains 7 files and 0 directories.
2024-10-05 06:55:49 - Total operations to perform: 14
2024-10-05 06:57:37 - Starting synchronization from C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source to C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica every 30 seconds
2024-10-05 06:57:37 - Source folder contains 7 files and 0 directories.
2024-10-05 06:57:37 - Replica folder contains 7 files and 0 directories.
2024-10-05 06:57:37 - Total operations to perform: 14
2024-10-05 06:59:22 - Starting synchronization from C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source to C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica every 30 seconds
2024-10-05 06:59:22 - Source folder contains 7 files and 0 directories.
2024-10-05 06:59:22 - Replica folder contains 7 files and 0 directories.
2024-10-05 06:59:22 - Total operations to perform: 14
2024-10-05 07:04:01 - Starting synchronization from C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source to C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica every 30 seconds
2024-10-05 07:04:01 - Source folder contains 7 files and 0 directories.
2024-10-05 07:04:01 - Replica folder contains 7 files and 0 directories.
2024-10-05 07:04:01 - Total operations to perform: 14
2024-10-05 07:04:01 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Added file1.odt
2024-10-05 07:04:01 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Added file1.odt -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Added file1.odt
2024-10-05 07:04:01 - Synchronization complete. Time taken: 0.10 seconds
2024-10-05 07:04:31 - Source folder contains 7 files and 0 directories.
2024-10-05 07:04:31 - Replica folder contains 7 files and 0 directories.
2024-10-05 07:04:31 - Total operations to perform: 14
2024-10-05 07:04:31 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 07:05:01 - Source folder contains 8 files and 0 directories.
2024-10-05 07:05:01 - Replica folder contains 7 files and 0 directories.
2024-10-05 07:05:01 - Total operations to perform: 15
2024-10-05 07:05:01 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New Microsoft Word Document.docx
2024-10-05 07:05:01 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New Microsoft Word Document.docx
2024-10-05 07:05:01 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 07:05:31 - Source folder contains 8 files and 0 directories.
2024-10-05 07:05:31 - Replica folder contains 7 files and 0 directories.
2024-10-05 07:05:31 - Total operations to perform: 15
2024-10-05 07:05:31 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New file 6 seems to be working.docx
2024-10-05 07:05:31 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New file 6 seems to be working.docx
2024-10-05 07:05:31 - Synchronization complete. Time taken: 0.02 seconds
2024-10-05 07:06:01 - Source folder contains 8 files and 0 directories.
2024-10-05 07:06:01 - Replica folder contains 7 files and 0 directories.
2024-10-05 07:06:01 - Total operations to perform: 15
2024-10-05 07:06:01 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New file 6 seems to be working.docx
2024-10-05 07:06:01 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New file 6 seems to be working.docx
2024-10-05 07:06:01 - Synchronization complete. Time taken: 0.03 seconds
2024-10-05 07:06:31 - Source folder contains 9 files and 0 directories.
2024-10-05 07:06:31 - Replica folder contains 7 files and 0 directories.
2024-10-05 07:06:31 - Total operations to perform: 16
2024-10-05 07:06:31 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.~lock.Added file1.odt#
2024-10-05 07:06:31 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\.~lock.Added file1.odt#
2024-10-05 07:06:31 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New file 6 seems to be working.docx
2024-10-05 07:06:31 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New file 6 seems to be working.docx
2024-10-05 07:06:31 - Synchronization complete. Time taken: 0.02 seconds
2024-10-05 07:07:01 - Source folder contains 8 files and 0 directories.
2024-10-05 07:07:01 - Replica folder contains 7 files and 0 directories.
2024-10-05 07:07:01 - Total operations to perform: 15
2024-10-05 07:07:01 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Added file1.odt
2024-10-05 07:07:01 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Added file1.odt -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Added file1.odt
2024-10-05 07:07:01 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New file 6 seems to be working.docx
2024-10-05 07:07:01 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New file 6 seems to be working.docx
2024-10-05 07:07:01 - Synchronization complete. Time taken: 0.02 seconds
2024-10-05 07:07:31 - Source folder contains 9 files and 0 directories.
2024-10-05 07:07:31 - Replica folder contains 7 files and 0 directories.
2024-10-05 07:07:31 - Total operations to perform: 16
2024-10-05 07:07:31 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New file 6 seems to be working.docx
2024-10-05 07:07:31 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New file 6 seems to be working.docx
2024-10-05 07:07:31 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New file 7.odt
2024-10-05 07:07:31 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New file 7.odt
2024-10-05 07:07:31 - Synchronization complete. Time taken: 0.02 seconds
2024-10-05 07:08:01 - Source folder contains 9 files and 0 directories.
2024-10-05 07:08:01 - Replica folder contains 1 files and 0 directories.
2024-10-05 07:08:01 - Total operations to perform: 10
2024-10-05 07:08:01 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\Added file1.odt
2024-10-05 07:08:01 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Added file1.odt
2024-10-05 07:08:01 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\Internal_Development_in_QA_(SDET)_Team_tesk_task.pdf
2024-10-05 07:08:01 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Internal_Development_in_QA_(SDET)_Team_tesk_task.pdf
2024-10-05 07:08:01 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New file 3 seems to be working fine finally.docx
2024-10-05 07:08:01 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New file 3 seems to be working fine finally.docx
2024-10-05 07:08:01 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New file 6 seems to be working.docx
2024-10-05 07:08:01 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New file 6 seems to be working.docx
2024-10-05 07:08:01 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New file 7.odt
2024-10-05 07:08:01 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New file 7.odt
2024-10-05 07:08:01 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\T1-1 Lis Announcements.xlsx
2024-10-05 07:08:01 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\T1-1 Lis Announcements.xlsx
2024-10-05 07:08:01 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\T3-21-2 Announcements.xlsx
2024-10-05 07:08:01 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\T3-21-2 Announcements.xlsx
2024-10-05 07:08:01 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\ttsMP3.com_VoiceText_2024-9-24_6-19-2.mp3
2024-10-05 07:08:01 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\ttsMP3.com_VoiceText_2024-9-24_6-19-2.mp3
2024-10-05 07:08:01 - Synchronization complete. Time taken: 0.02 seconds
2024-10-05 07:08:31 - Source folder contains 9 files and 0 directories.
2024-10-05 07:08:31 - Replica folder contains 1 files and 0 directories.
2024-10-05 07:08:31 - Total operations to perform: 10
2024-10-05 07:08:31 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\Added file1.odt
2024-10-05 07:08:31 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Added file1.odt
2024-10-05 07:08:31 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\Internal_Development_in_QA_(SDET)_Team_tesk_task.pdf
2024-10-05 07:08:31 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Internal_Development_in_QA_(SDET)_Team_tesk_task.pdf
2024-10-05 07:08:31 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New file 3 seems to be working fine finally.docx
2024-10-05 07:08:31 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New file 3 seems to be working fine finally.docx
2024-10-05 07:08:31 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New file 6 seems to be working.docx
2024-10-05 07:08:31 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New file 6 seems to be working.docx
2024-10-05 07:08:31 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New file 7.odt
2024-10-05 07:08:31 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New file 7.odt
2024-10-05 07:08:31 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\T1-1 Lis Announcements.xlsx
2024-10-05 07:08:31 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\T1-1 Lis Announcements.xlsx
2024-10-05 07:08:31 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\T3-21-2 Announcements.xlsx
2024-10-05 07:08:31 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\T3-21-2 Announcements.xlsx
2024-10-05 07:08:31 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\ttsMP3.com_VoiceText_2024-9-24_6-19-2.mp3
2024-10-05 07:08:31 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\ttsMP3.com_VoiceText_2024-9-24_6-19-2.mp3
2024-10-05 07:08:31 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 07:08:47 - Received interrupt signal. Exiting gracefully...
2024-10-05 07:26:29 - Starting synchronization from C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source to C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica every 30 seconds
2024-10-05 07:26:29 - Source folder contains 9 files and 0 directories.
2024-10-05 07:26:29 - Replica folder contains 1 files and 0 directories.
2024-10-05 07:26:29 - Total operations to perform: 10
2024-10-05 07:26:29 - Synchronization complete. Time taken: 0.00 seconds
2024-10-05 07:26:59 - Source folder contains 9 files and 0 directories.
2024-10-05 07:26:59 - Replica folder contains 1 files and 0 directories.
2024-10-05 07:26:59 - Total operations to perform: 10
2024-10-05 07:26:59 - Synchronization complete. Time taken: 0.00 seconds
2024-10-05 07:27:29 - Source folder contains 9 files and 0 directories.
2024-10-05 07:27:29 - Replica folder contains 1 files and 0 directories.
2024-10-05 07:27:29 - Total operations to perform: 10
2024-10-05 07:27:29 - Synchronization complete. Time taken: 0.00 seconds
2024-10-05 07:27:59 - Source folder contains 9 files and 0 directories.
2024-10-05 07:27:59 - Replica folder contains 1 files and 0 directories.
2024-10-05 07:27:59 - Total operations to perform: 10
2024-10-05 07:27:59 - Synchronization complete. Time taken: 0.00 seconds
2024-10-05 07:28:29 - Source folder contains 9 files and 0 directories.
2024-10-05 07:28:29 - Replica folder contains 1 files and 0 directories.
2024-10-05 07:28:29 - Total operations to perform: 10
2024-10-05 07:28:29 - Synchronization complete. Time taken: 0.00 seconds
2024-10-05 07:28:59 - Source folder contains 9 files and 0 directories.
2024-10-05 07:28:59 - Replica folder contains 1 files and 0 directories.
2024-10-05 07:28:59 - Total operations to perform: 10
2024-10-05 07:28:59 - Synchronization complete. Time taken: 0.00 seconds
2024-10-05 07:29:29 - Source folder contains 9 files and 0 directories.
2024-10-05 07:29:29 - Replica folder contains 1 files and 0 directories.
2024-10-05 07:29:29 - Total operations to perform: 10
2024-10-05 07:29:29 - Synchronization complete. Time taken: 0.00 seconds
2024-10-05 07:29:59 - Source folder contains 9 files and 0 directories.
2024-10-05 07:29:59 - Replica folder contains 1 files and 0 directories.
2024-10-05 07:29:59 - Total operations to perform: 10
2024-10-05 07:29:59 - Synchronization complete. Time taken: 0.00 seconds
2024-10-05 07:30:29 - Source folder contains 9 files and 0 directories.
2024-10-05 07:30:29 - Replica folder contains 1 files and 0 directories.
2024-10-05 07:30:29 - Total operations to perform: 10
2024-10-05 07:30:29 - Synchronization complete. Time taken: 0.00 seconds
2024-10-05 07:30:49 - Received interrupt signal. Exiting gracefully...
2024-10-05 07:31:08 - Starting synchronization from C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source to C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica every 30 seconds
2024-10-05 07:31:08 - Source folder contains 9 files and 0 directories.
2024-10-05 07:31:08 - Replica folder contains 1 files and 0 directories.
2024-10-05 07:31:08 - Total operations to perform: 10
2024-10-05 07:31:08 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\ttsMP3.com_VoiceText_2024-9-24_6-19-2.mp3
2024-10-05 07:31:08 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\ttsMP3.com_VoiceText_2024-9-24_6-19-2.mp3 -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\ttsMP3.com_VoiceText_2024-9-24_6-19-2.mp3
2024-10-05 07:31:08 - Synchronization complete. Time taken: 0.06 seconds
2024-10-05 07:31:38 - Source folder contains 9 files and 0 directories.
2024-10-05 07:31:38 - Replica folder contains 2 files and 0 directories.
2024-10-05 07:31:38 - Total operations to perform: 11
2024-10-05 07:31:38 - Synchronization complete. Time taken: 0.00 seconds
2024-10-05 07:32:08 - Source folder contains 10 files and 0 directories.
2024-10-05 07:32:08 - Replica folder contains 2 files and 0 directories.
2024-10-05 07:32:08 - Total operations to perform: 12
2024-10-05 07:32:08 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Where are the others.odt
2024-10-05 07:32:08 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Where are the others.odt -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Where are the others.odt
2024-10-05 07:32:08 - Synchronization complete. Time taken: 0.00 seconds
2024-10-05 07:32:38 - Source folder contains 1 files and 0 directories.
2024-10-05 07:32:38 - Replica folder contains 3 files and 0 directories.
2024-10-05 07:32:38 - Total operations to perform: 4
2024-10-05 07:32:38 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\ttsMP3.com_VoiceText_2024-9-24_6-19-2.mp3
2024-10-05 07:32:38 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\.\ttsMP3.com_VoiceText_2024-9-24_6-19-2.mp3
2024-10-05 07:32:38 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Where are the others.odt
2024-10-05 07:32:38 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\.\Where are the others.odt
2024-10-05 07:32:38 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 07:33:08 - Source folder contains 4 files and 0 directories.
2024-10-05 07:33:08 - Replica folder contains 3 files and 0 directories.
2024-10-05 07:33:08 - Total operations to perform: 7
2024-10-05 07:33:08 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New 3.xlsx
2024-10-05 07:33:08 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\New 3.xlsx -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New 3.xlsx
2024-10-05 07:33:08 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\ttsMP3.com_VoiceText_2024-9-24_6-19-2.mp3
2024-10-05 07:33:08 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\.\ttsMP3.com_VoiceText_2024-9-24_6-19-2.mp3
2024-10-05 07:33:08 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Where are the others.odt
2024-10-05 07:33:08 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\.\Where are the others.odt
2024-10-05 07:33:08 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 07:33:38 - Source folder contains 9 files and 0 directories.
2024-10-05 07:33:38 - Replica folder contains 4 files and 0 directories.
2024-10-05 07:33:38 - Total operations to perform: 13
2024-10-05 07:33:38 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\T3-21 Canva - Sheet1.csv
2024-10-05 07:33:38 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\T3-21 Canva - Sheet1.csv -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\T3-21 Canva - Sheet1.csv
2024-10-05 07:33:38 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\ttsMP3.com_VoiceText_2024-9-24_6-19-2.mp3
2024-10-05 07:33:38 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\.\ttsMP3.com_VoiceText_2024-9-24_6-19-2.mp3
2024-10-05 07:33:38 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Where are the others.odt
2024-10-05 07:33:38 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\.\Where are the others.odt
2024-10-05 07:33:38 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 07:34:08 - Source folder contains 9 files and 0 directories.
2024-10-05 07:34:08 - Replica folder contains 5 files and 0 directories.
2024-10-05 07:34:08 - Total operations to perform: 14
2024-10-05 07:34:08 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\ttsMP3.com_VoiceText_2024-9-24_6-19-2.mp3
2024-10-05 07:34:08 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\.\ttsMP3.com_VoiceText_2024-9-24_6-19-2.mp3
2024-10-05 07:34:08 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Where are the others.odt
2024-10-05 07:34:08 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\.\Where are the others.odt
2024-10-05 07:34:08 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 07:34:38 - Source folder contains 9 files and 0 directories.
2024-10-05 07:34:38 - Replica folder contains 5 files and 0 directories.
2024-10-05 07:34:38 - Total operations to perform: 14
2024-10-05 07:34:38 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\ttsMP3.com_VoiceText_2024-9-24_6-19-2.mp3
2024-10-05 07:34:38 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\.\ttsMP3.com_VoiceText_2024-9-24_6-19-2.mp3
2024-10-05 07:34:38 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Where are the others.odt
2024-10-05 07:34:38 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\.\Where are the others.odt
2024-10-05 07:34:38 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 07:35:08 - Source folder contains 9 files and 0 directories.
2024-10-05 07:35:08 - Replica folder contains 5 files and 0 directories.
2024-10-05 07:35:08 - Total operations to perform: 14
2024-10-05 07:35:08 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\ttsMP3.com_VoiceText_2024-9-24_6-19-2.mp3
2024-10-05 07:35:08 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\.\ttsMP3.com_VoiceText_2024-9-24_6-19-2.mp3
2024-10-05 07:35:08 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Where are the others.odt
2024-10-05 07:35:08 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\.\Where are the others.odt
2024-10-05 07:35:08 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 07:35:38 - Source folder contains 9 files and 0 directories.
2024-10-05 07:35:38 - Replica folder contains 5 files and 0 directories.
2024-10-05 07:35:38 - Total operations to perform: 14
2024-10-05 07:35:38 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\ttsMP3.com_VoiceText_2024-9-24_6-19-2.mp3
2024-10-05 07:35:38 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\.\ttsMP3.com_VoiceText_2024-9-24_6-19-2.mp3
2024-10-05 07:35:38 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Where are the others.odt
2024-10-05 07:35:38 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\.\Where are the others.odt
2024-10-05 07:35:38 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 07:36:08 - Source folder contains 9 files and 0 directories.
2024-10-05 07:36:08 - Replica folder contains 5 files and 0 directories.
2024-10-05 07:36:08 - Total operations to perform: 14
2024-10-05 07:36:08 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\ttsMP3.com_VoiceText_2024-9-24_6-19-2.mp3
2024-10-05 07:36:08 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\.\ttsMP3.com_VoiceText_2024-9-24_6-19-2.mp3
2024-10-05 07:36:08 - Path does not exist: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Where are the others.odt
2024-10-05 07:36:08 - Skipping potentially unsafe file path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\.\Where are the others.odt
2024-10-05 07:36:08 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 07:36:12 - Received interrupt signal. Exiting gracefully...
2024-10-05 07:40:15 - Starting synchronization from C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source to C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica every 30 seconds
2024-10-05 07:40:15 - Source folder contains 9 files and 0 directories.
2024-10-05 07:40:15 - Replica folder contains 5 files and 0 directories.
2024-10-05 07:40:15 - Total operations to perform: 14
2024-10-05 07:40:15 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\1727131602042kpvah2po-voicemaker.in-speech.mp3
2024-10-05 07:40:15 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\1727131602042kpvah2po-voicemaker.in-speech.mp3 -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\1727131602042kpvah2po-voicemaker.in-speech.mp3
2024-10-05 07:40:15 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\1727131749681w8k0to7a-voicemaker.in-speech.mp3
2024-10-05 07:40:15 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\1727131749681w8k0to7a-voicemaker.in-speech.mp3 -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\1727131749681w8k0to7a-voicemaker.in-speech.mp3
2024-10-05 07:40:15 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New 1.docx
2024-10-05 07:40:15 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\New 1.docx -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New 1.docx
2024-10-05 07:40:15 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New 2.odt
2024-10-05 07:40:15 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\New 2.odt -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New 2.odt
2024-10-05 07:40:15 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Spotit T2-11ZH.pdf
2024-10-05 07:40:15 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Spotit T2-11ZH.pdf -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Spotit T2-11ZH.pdf
2024-10-05 07:40:15 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\T1-01 Reorder.xlsx
2024-10-05 07:40:15 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\T1-01 Reorder.xlsx -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\T1-01 Reorder.xlsx
2024-10-05 07:40:15 - File removed: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\ttsMP3.com_VoiceText_2024-9-24_6-19-2.mp3
2024-10-05 07:40:15 - File removed: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\Where are the others.odt
2024-10-05 07:40:15 - Synchronization complete. Time taken: 0.09 seconds
2024-10-05 07:40:45 - Source folder contains 10 files and 0 directories.
2024-10-05 07:40:45 - Replica folder contains 9 files and 0 directories.
2024-10-05 07:40:45 - Total operations to perform: 19
2024-10-05 07:40:45 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New Microsoft Word Document.docx
2024-10-05 07:40:45 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\New Microsoft Word Document.docx -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New Microsoft Word Document.docx
2024-10-05 07:40:45 - Synchronization complete. Time taken: 0.02 seconds
2024-10-05 07:41:15 - Source folder contains 10 files and 0 directories.
2024-10-05 07:41:15 - Replica folder contains 10 files and 0 directories.
2024-10-05 07:41:15 - Total operations to perform: 20
2024-10-05 07:41:15 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Fingers crossed.docx
2024-10-05 07:41:15 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Fingers crossed.docx -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Fingers crossed.docx
2024-10-05 07:41:15 - File removed: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New Microsoft Word Document.docx
2024-10-05 07:41:15 - Synchronization complete. Time taken: 0.02 seconds
2024-10-05 07:41:45 - Source folder contains 10 files and 0 directories.
2024-10-05 07:41:45 - Replica folder contains 10 files and 0 directories.
2024-10-05 07:41:45 - Total operations to perform: 20
2024-10-05 07:41:45 - Synchronization complete. Time taken: 0.02 seconds
2024-10-05 07:42:15 - Source folder contains 10 files and 0 directories.
2024-10-05 07:42:15 - Replica folder contains 10 files and 0 directories.
2024-10-05 07:42:15 - Total operations to perform: 20
2024-10-05 07:42:15 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 07:42:45 - Source folder contains 7 files and 0 directories.
2024-10-05 07:42:45 - Replica folder contains 10 files and 0 directories.
2024-10-05 07:42:45 - Total operations to perform: 17
2024-10-05 07:42:45 - File removed: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\Spotit T2-11ZH.pdf
2024-10-05 07:42:45 - File removed: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\T1-01 Reorder.xlsx
2024-10-05 07:42:45 - File removed: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\T3-21 Canva - Sheet1.csv
2024-10-05 07:42:45 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 07:43:15 - Source folder contains 7 files and 0 directories.
2024-10-05 07:43:15 - Replica folder contains 1 files and 0 directories.
2024-10-05 07:43:15 - Total operations to perform: 8
2024-10-05 07:43:15 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\1727131602042kpvah2po-voicemaker.in-speech.mp3
2024-10-05 07:43:15 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\1727131602042kpvah2po-voicemaker.in-speech.mp3 -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\1727131602042kpvah2po-voicemaker.in-speech.mp3
2024-10-05 07:43:15 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\1727131749681w8k0to7a-voicemaker.in-speech.mp3
2024-10-05 07:43:15 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\1727131749681w8k0to7a-voicemaker.in-speech.mp3 -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\1727131749681w8k0to7a-voicemaker.in-speech.mp3
2024-10-05 07:43:15 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Fingers crossed.docx
2024-10-05 07:43:15 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Fingers crossed.docx -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Fingers crossed.docx
2024-10-05 07:43:15 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New 1.docx
2024-10-05 07:43:15 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\New 1.docx -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New 1.docx
2024-10-05 07:43:15 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New 2.odt
2024-10-05 07:43:15 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\New 2.odt -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New 2.odt
2024-10-05 07:43:15 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New 3.xlsx
2024-10-05 07:43:15 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\New 3.xlsx -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New 3.xlsx
2024-10-05 07:43:15 - Synchronization complete. Time taken: 0.03 seconds
2024-10-05 07:43:45 - Source folder contains 8 files and 0 directories.
2024-10-05 07:43:45 - Replica folder contains 7 files and 0 directories.
2024-10-05 07:43:45 - Total operations to perform: 15
2024-10-05 07:43:45 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\.~lock.New 2.odt#
2024-10-05 07:43:45 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\.~lock.New 2.odt# -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\.~lock.New 2.odt#
2024-10-05 07:43:45 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New 2.odt
2024-10-05 07:43:45 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\New 2.odt -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New 2.odt
2024-10-05 07:43:45 - Synchronization complete. Time taken: 0.02 seconds
2024-10-05 07:44:15 - Source folder contains 7 files and 0 directories.
2024-10-05 07:44:15 - Replica folder contains 8 files and 0 directories.
2024-10-05 07:44:15 - Total operations to perform: 15
2024-10-05 07:44:15 - File removed: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.~lock.New 2.odt#
2024-10-05 07:44:15 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 07:44:45 - Source folder contains 7 files and 0 directories.
2024-10-05 07:44:45 - Replica folder contains 7 files and 0 directories.
2024-10-05 07:44:45 - Total operations to perform: 14
2024-10-05 07:44:45 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New 2.odt
2024-10-05 07:44:45 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\New 2.odt -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New 2.odt
2024-10-05 07:44:45 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 07:45:15 - Source folder contains 8 files and 0 directories.
2024-10-05 07:45:15 - Replica folder contains 7 files and 0 directories.
2024-10-05 07:45:15 - Total operations to perform: 15
2024-10-05 07:45:15 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New Microsoft Word Document.docx
2024-10-05 07:45:15 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\New Microsoft Word Document.docx -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New Microsoft Word Document.docx
2024-10-05 07:45:15 - Synchronization complete. Time taken: 0.02 seconds
2024-10-05 07:45:45 - Source folder contains 8 files and 1 directories.
2024-10-05 07:45:45 - Replica folder contains 8 files and 0 directories.
2024-10-05 07:45:45 - Total operations to perform: 17
2024-10-05 07:45:45 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\How about this one.docx
2024-10-05 07:45:45 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\How about this one.docx -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\How about this one.docx
2024-10-05 07:45:45 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\Trial folder
2024-10-05 07:45:45 - Directory created: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\Trial folder
2024-10-05 07:45:45 - File removed: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New Microsoft Word Document.docx
2024-10-05 07:45:45 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 07:46:15 - Source folder contains 9 files and 1 directories.
2024-10-05 07:46:15 - Replica folder contains 8 files and 1 directories.
2024-10-05 07:46:15 - Total operations to perform: 19
2024-10-05 07:46:15 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New shortcut.lnk
2024-10-05 07:46:15 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\New shortcut.lnk -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New shortcut.lnk
2024-10-05 07:46:15 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 07:46:45 - Source folder contains 10 files and 1 directories.
2024-10-05 07:46:45 - Replica folder contains 9 files and 1 directories.
2024-10-05 07:46:45 - Total operations to perform: 21
2024-10-05 07:46:45 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Trial for a shortcut RSP 100 (2023).lnk
2024-10-05 07:46:45 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Trial for a shortcut RSP 100 (2023).lnk -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Trial for a shortcut RSP 100 (2023).lnk
2024-10-05 07:46:45 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\Trial folder\New Bitmap image.bmp
2024-10-05 07:46:45 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Trial folder\New Bitmap image.bmp -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\Trial folder\New Bitmap image.bmp
2024-10-05 07:46:45 - File removed: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New shortcut.lnk
2024-10-05 07:46:45 - Synchronization complete. Time taken: 0.02 seconds
2024-10-05 07:47:15 - Source folder contains 11 files and 1 directories.
2024-10-05 07:47:15 - Replica folder contains 10 files and 1 directories.
2024-10-05 07:47:15 - Total operations to perform: 23
2024-10-05 07:47:15 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Works like a charm.odg
2024-10-05 07:47:15 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Works like a charm.odg -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Works like a charm.odg
2024-10-05 07:47:15 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\Trial folder\Image trial 1.bmp
2024-10-05 07:47:15 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Trial folder\Image trial 1.bmp -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\Trial folder\Image trial 1.bmp
2024-10-05 07:47:15 - File removed: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\Trial folder\New Bitmap image.bmp
2024-10-05 07:47:15 - Synchronization complete. Time taken: 0.02 seconds
2024-10-05 07:47:45 - Source folder contains 13 files and 1 directories.
2024-10-05 07:47:45 - Replica folder contains 11 files and 1 directories.
2024-10-05 07:47:45 - Total operations to perform: 26
2024-10-05 07:47:45 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\I belive I can fly.odp
2024-10-05 07:47:45 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\I belive I can fly.odp -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\I belive I can fly.odp
2024-10-05 07:47:45 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Numbers numbers.ods
2024-10-05 07:47:45 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Numbers numbers.ods -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Numbers numbers.ods
2024-10-05 07:47:45 - Synchronization complete. Time taken: 0.02 seconds
2024-10-05 07:48:15 - Source folder contains 16 files and 1 directories.
2024-10-05 07:48:15 - Replica folder contains 13 files and 1 directories.
2024-10-05 07:48:15 - Total operations to perform: 31
2024-10-05 07:48:15 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New Microsoft Publisher Document.pub
2024-10-05 07:48:15 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\New Microsoft Publisher Document.pub -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New Microsoft Publisher Document.pub
2024-10-05 07:48:15 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New OpenDocument Text.odt
2024-10-05 07:48:15 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\New OpenDocument Text.odt -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New OpenDocument Text.odt
2024-10-05 07:48:15 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New OpenOffice.Pptx.pptx
2024-10-05 07:48:15 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\New OpenOffice.Pptx.pptx -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New OpenOffice.Pptx.pptx
2024-10-05 07:48:15 - Synchronization complete. Time taken: 0.02 seconds
2024-10-05 07:48:45 - Source folder contains 18 files and 1 directories.
2024-10-05 07:48:45 - Replica folder contains 16 files and 1 directories.
2024-10-05 07:48:45 - Total operations to perform: 36
2024-10-05 07:48:45 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New Microsoft Excel Worksheet.xlsx
2024-10-05 07:48:45 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\New Microsoft Excel Worksheet.xlsx -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New Microsoft Excel Worksheet.xlsx
2024-10-05 07:48:45 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New Text Document.txt
2024-10-05 07:48:45 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\New Text Document.txt -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New Text Document.txt
2024-10-05 07:48:45 - Synchronization complete. Time taken: 0.02 seconds
2024-10-05 07:49:15 - Source folder contains 18 files and 1 directories.
2024-10-05 07:49:15 - Replica folder contains 18 files and 1 directories.
2024-10-05 07:49:15 - Total operations to perform: 38
2024-10-05 07:49:15 - Synchronization complete. Time taken: 0.02 seconds
2024-10-05 07:49:45 - Source folder contains 3 files and 1 directories.
2024-10-05 07:49:45 - Replica folder contains 18 files and 1 directories.
2024-10-05 07:49:45 - Total operations to perform: 23
2024-10-05 07:49:45 - File removed: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\1727131602042kpvah2po-voicemaker.in-speech.mp3
2024-10-05 07:49:45 - File removed: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\1727131749681w8k0to7a-voicemaker.in-speech.mp3
2024-10-05 07:49:45 - File removed: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\Fingers crossed.docx
2024-10-05 07:49:45 - File removed: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\How about this one.docx
2024-10-05 07:49:45 - File removed: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\I belive I can fly.odp
2024-10-05 07:49:45 - File removed: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New 1.docx
2024-10-05 07:49:45 - File removed: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New 2.odt
2024-10-05 07:49:45 - File removed: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New 3.xlsx
2024-10-05 07:49:45 - File removed: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New Microsoft Excel Worksheet.xlsx
2024-10-05 07:49:45 - File removed: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New Microsoft Publisher Document.pub
2024-10-05 07:49:45 - File removed: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New OpenDocument Text.odt
2024-10-05 07:49:45 - File removed: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New OpenOffice.Pptx.pptx
2024-10-05 07:49:45 - File removed: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New Text Document.txt
2024-10-05 07:49:45 - File removed: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\Numbers numbers.ods
2024-10-05 07:49:45 - File removed: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\Trial for a shortcut RSP 100 (2023).lnk
2024-10-05 07:49:45 - Synchronization complete. Time taken: 0.02 seconds
2024-10-05 07:50:15 - Source folder contains 3 files and 1 directories.
2024-10-05 07:50:15 - Replica folder contains 1 files and 0 directories.
2024-10-05 07:50:15 - Total operations to perform: 5
2024-10-05 07:50:15 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Works like a charm.odg
2024-10-05 07:50:15 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Works like a charm.odg -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Works like a charm.odg
2024-10-05 07:50:15 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\Trial folder
2024-10-05 07:50:15 - Directory created: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\Trial folder
2024-10-05 07:50:15 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\Trial folder\Image trial 1.bmp
2024-10-05 07:50:15 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Trial folder\Image trial 1.bmp -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\Trial folder\Image trial 1.bmp
2024-10-05 07:50:15 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 07:50:45 - Source folder contains 3 files and 1 directories.
2024-10-05 07:50:45 - Replica folder contains 3 files and 1 directories.
2024-10-05 07:50:45 - Total operations to perform: 8
2024-10-05 07:50:45 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 07:51:15 - Source folder contains 3 files and 1 directories.
2024-10-05 07:51:15 - Replica folder contains 3 files and 1 directories.
2024-10-05 07:51:15 - Total operations to perform: 8
2024-10-05 07:51:15 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 07:51:45 - Source folder contains 3 files and 1 directories.
2024-10-05 07:51:45 - Replica folder contains 3 files and 1 directories.
2024-10-05 07:51:45 - Total operations to perform: 8
2024-10-05 07:51:45 - Synchronization complete. Time taken: 0.00 seconds
2024-10-05 07:52:15 - Source folder contains 3 files and 1 directories.
2024-10-05 07:52:15 - Replica folder contains 3 files and 1 directories.
2024-10-05 07:52:15 - Total operations to perform: 8
2024-10-05 07:52:15 - Synchronization complete. Time taken: 0.00 seconds
2024-10-05 07:52:18 - Received interrupt signal. Exiting gracefully...
2024-10-05 08:02:32 - Starting synchronization from C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source to C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica every 30 seconds
2024-10-05 08:02:32 - Source folder contains 3 files and 1 directories.
2024-10-05 08:02:32 - Replica folder contains 3 files and 1 directories.
2024-10-05 08:02:32 - Total operations to perform: 8
2024-10-05 08:02:32 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:03:02 - Source folder contains 4 files and 1 directories.
2024-10-05 08:03:02 - Replica folder contains 3 files and 1 directories.
2024-10-05 08:03:02 - Total operations to perform: 9
2024-10-05 08:03:02 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New OpenDocument Text.odt
2024-10-05 08:03:02 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\New OpenDocument Text.odt -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New OpenDocument Text.odt
2024-10-05 08:03:02 - Synchronization complete. Time taken: 0.07 seconds
2024-10-05 08:03:32 - Source folder contains 5 files and 1 directories.
2024-10-05 08:03:32 - Replica folder contains 4 files and 1 directories.
2024-10-05 08:03:32 - Total operations to perform: 11
2024-10-05 08:03:32 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Second Trial after a graceful exit.odt
2024-10-05 08:03:32 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Second Trial after a graceful exit.odt -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Second Trial after a graceful exit.odt
2024-10-05 08:03:32 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:04:02 - Source folder contains 5 files and 1 directories.
2024-10-05 08:04:02 - Replica folder contains 5 files and 1 directories.
2024-10-05 08:04:02 - Total operations to perform: 12
2024-10-05 08:04:02 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Seems to be tickity boo.odt
2024-10-05 08:04:02 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Seems to be tickity boo.odt -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Seems to be tickity boo.odt
2024-10-05 08:04:02 - File removed: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\New OpenDocument Text.odt
2024-10-05 08:04:02 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:04:32 - Source folder contains 5 files and 1 directories.
2024-10-05 08:04:32 - Replica folder contains 5 files and 1 directories.
2024-10-05 08:04:32 - Total operations to perform: 12
2024-10-05 08:04:32 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Seems to be tickety-boo.odt
2024-10-05 08:04:32 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Seems to be tickety-boo.odt -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Seems to be tickety-boo.odt
2024-10-05 08:04:32 - File removed: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\Seems to be tickity boo.odt
2024-10-05 08:04:32 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:05:02 - Source folder contains 6 files and 1 directories.
2024-10-05 08:05:02 - Replica folder contains 5 files and 1 directories.
2024-10-05 08:05:02 - Total operations to perform: 13
2024-10-05 08:05:02 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\.~lock.Seems to be tickety-boo.odt#
2024-10-05 08:05:02 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\.~lock.Seems to be tickety-boo.odt# -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\.~lock.Seems to be tickety-boo.odt#
2024-10-05 08:05:02 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Seems to be tickety-boo.odt
2024-10-05 08:05:02 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Seems to be tickety-boo.odt -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Seems to be tickety-boo.odt
2024-10-05 08:05:02 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:05:32 - Source folder contains 5 files and 1 directories.
2024-10-05 08:05:32 - Replica folder contains 6 files and 1 directories.
2024-10-05 08:05:32 - Total operations to perform: 13
2024-10-05 08:05:32 - Error copying file C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Seems to be tickety-boo.odt to C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Seems to be tickety-boo.odt: [WinError 32] The process cannot access the file because it is being used by another process
2024-10-05 08:05:32 - File removed: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.~lock.Seems to be tickety-boo.odt#
2024-10-05 08:05:32 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:06:02 - Source folder contains 5 files and 1 directories.
2024-10-05 08:06:02 - Replica folder contains 6 files and 1 directories.
2024-10-05 08:06:02 - Total operations to perform: 13
2024-10-05 08:06:02 - Error copying file C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Seems to be tickety-boo.odt to C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Seems to be tickety-boo.odt: [WinError 32] The process cannot access the file because it is being used by another process
2024-10-05 08:06:02 - File removed: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.~lock.Seems to be tickety-boo.odt#
2024-10-05 08:06:02 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:06:32 - Source folder contains 5 files and 1 directories.
2024-10-05 08:06:32 - Replica folder contains 5 files and 1 directories.
2024-10-05 08:06:32 - Total operations to perform: 12
2024-10-05 08:06:32 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Seems to be tickety-boo.odt
2024-10-05 08:06:32 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Seems to be tickety-boo.odt -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Seems to be tickety-boo.odt
2024-10-05 08:06:32 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:07:02 - Source folder contains 5 files and 1 directories.
2024-10-05 08:07:02 - Replica folder contains 5 files and 1 directories.
2024-10-05 08:07:02 - Total operations to perform: 12
2024-10-05 08:07:02 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:07:32 - Source folder contains 5 files and 1 directories.
2024-10-05 08:07:32 - Replica folder contains 5 files and 1 directories.
2024-10-05 08:07:32 - Total operations to perform: 12
2024-10-05 08:07:32 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:08:02 - Source folder contains 5 files and 1 directories.
2024-10-05 08:08:02 - Replica folder contains 5 files and 1 directories.
2024-10-05 08:08:02 - Total operations to perform: 12
2024-10-05 08:08:02 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:08:32 - Source folder contains 5 files and 1 directories.
2024-10-05 08:08:32 - Replica folder contains 5 files and 1 directories.
2024-10-05 08:08:32 - Total operations to perform: 12
2024-10-05 08:08:32 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:09:02 - Source folder contains 5 files and 1 directories.
2024-10-05 08:09:02 - Replica folder contains 5 files and 1 directories.
2024-10-05 08:09:02 - Total operations to perform: 12
2024-10-05 08:09:02 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:09:32 - Source folder contains 5 files and 1 directories.
2024-10-05 08:09:32 - Replica folder contains 5 files and 1 directories.
2024-10-05 08:09:32 - Total operations to perform: 12
2024-10-05 08:09:32 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:10:02 - Source folder contains 5 files and 1 directories.
2024-10-05 08:10:02 - Replica folder contains 5 files and 1 directories.
2024-10-05 08:10:02 - Total operations to perform: 12
2024-10-05 08:10:02 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:10:32 - Source folder contains 5 files and 1 directories.
2024-10-05 08:10:32 - Replica folder contains 5 files and 1 directories.
2024-10-05 08:10:32 - Total operations to perform: 12
2024-10-05 08:10:32 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:11:02 - Source folder contains 5 files and 1 directories.
2024-10-05 08:11:02 - Replica folder contains 5 files and 1 directories.
2024-10-05 08:11:02 - Total operations to perform: 12
2024-10-05 08:11:02 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:11:32 - Source folder contains 5 files and 1 directories.
2024-10-05 08:11:32 - Replica folder contains 5 files and 1 directories.
2024-10-05 08:11:32 - Total operations to perform: 12
2024-10-05 08:11:32 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:12:02 - Source folder contains 5 files and 1 directories.
2024-10-05 08:12:02 - Replica folder contains 5 files and 1 directories.
2024-10-05 08:12:02 - Total operations to perform: 12
2024-10-05 08:12:02 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:12:32 - Source folder contains 5 files and 1 directories.
2024-10-05 08:12:32 - Replica folder contains 5 files and 1 directories.
2024-10-05 08:12:32 - Total operations to perform: 12
2024-10-05 08:12:32 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:13:02 - Source folder contains 5 files and 1 directories.
2024-10-05 08:13:02 - Replica folder contains 5 files and 1 directories.
2024-10-05 08:13:02 - Total operations to perform: 12
2024-10-05 08:13:02 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:13:32 - Source folder contains 5 files and 1 directories.
2024-10-05 08:13:32 - Replica folder contains 5 files and 1 directories.
2024-10-05 08:13:32 - Total operations to perform: 12
2024-10-05 08:13:32 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:14:02 - Source folder contains 5 files and 1 directories.
2024-10-05 08:14:02 - Replica folder contains 5 files and 1 directories.
2024-10-05 08:14:02 - Total operations to perform: 12
2024-10-05 08:14:02 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:14:32 - Source folder contains 5 files and 1 directories.
2024-10-05 08:14:32 - Replica folder contains 5 files and 1 directories.
2024-10-05 08:14:32 - Total operations to perform: 12
2024-10-05 08:14:32 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:15:02 - Source folder contains 5 files and 1 directories.
2024-10-05 08:15:02 - Replica folder contains 5 files and 1 directories.
2024-10-05 08:15:02 - Total operations to perform: 12
2024-10-05 08:15:02 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:15:32 - Source folder contains 5 files and 1 directories.
2024-10-05 08:15:32 - Replica folder contains 5 files and 1 directories.
2024-10-05 08:15:32 - Total operations to perform: 12
2024-10-05 08:15:32 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:16:02 - Source folder contains 5 files and 1 directories.
2024-10-05 08:16:02 - Replica folder contains 5 files and 1 directories.
2024-10-05 08:16:02 - Total operations to perform: 12
2024-10-05 08:16:02 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:21:05 - Starting synchronization from C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source to C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica every 30 seconds
2024-10-05 08:21:05 - Source folder contains 5 files and 1 directories.
2024-10-05 08:21:05 - Replica folder contains 5 files and 1 directories.
2024-10-05 08:21:05 - Total operations to perform: 12
2024-10-05 08:21:05 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:21:35 - Source folder contains 6 files and 1 directories.
2024-10-05 08:21:35 - Replica folder contains 5 files and 1 directories.
2024-10-05 08:21:35 - Total operations to perform: 13
2024-10-05 08:21:35 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New File after a restart.docx
2024-10-05 08:21:35 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\New File after a restart.docx -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New File after a restart.docx
2024-10-05 08:21:35 - Synchronization complete. Time taken: 0.08 seconds
2024-10-05 08:22:05 - Source folder contains 7 files and 1 directories.
2024-10-05 08:22:05 - Replica folder contains 6 files and 1 directories.
2024-10-05 08:22:05 - Total operations to perform: 15
2024-10-05 08:22:05 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\Trial folder\New Excel after a restart.xlsx
2024-10-05 08:22:05 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Trial folder\New Excel after a restart.xlsx -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\Trial folder\New Excel after a restart.xlsx
2024-10-05 08:22:05 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:22:35 - Source folder contains 8 files and 1 directories.
2024-10-05 08:22:35 - Replica folder contains 7 files and 1 directories.
2024-10-05 08:22:35 - Total operations to perform: 17
2024-10-05 08:22:35 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\.~lock.Seems to be tickety-boo.odt#
2024-10-05 08:22:35 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\.~lock.Seems to be tickety-boo.odt# -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\.~lock.Seems to be tickety-boo.odt#
2024-10-05 08:22:35 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:23:05 - Source folder contains 7 files and 1 directories.
2024-10-05 08:23:05 - Replica folder contains 7 files and 1 directories.
2024-10-05 08:23:05 - Total operations to perform: 16
2024-10-05 08:23:05 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Seems to be tickety-boo.odt
2024-10-05 08:23:05 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Seems to be tickety-boo.odt -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Seems to be tickety-boo.odt
2024-10-05 08:23:05 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:23:35 - Source folder contains 7 files and 1 directories.
2024-10-05 08:23:35 - Replica folder contains 1 files and 0 directories.
2024-10-05 08:23:35 - Total operations to perform: 9
2024-10-05 08:23:35 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New File after a restart.docx
2024-10-05 08:23:35 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\New File after a restart.docx -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\New File after a restart.docx
2024-10-05 08:23:35 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Second Trial after a graceful exit.odt
2024-10-05 08:23:35 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Second Trial after a graceful exit.odt -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Second Trial after a graceful exit.odt
2024-10-05 08:23:35 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Seems to be tickety-boo.odt
2024-10-05 08:23:35 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Seems to be tickety-boo.odt -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Seems to be tickety-boo.odt
2024-10-05 08:23:35 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Works like a charm.odg
2024-10-05 08:23:35 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Works like a charm.odg -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\.\Works like a charm.odg
2024-10-05 08:23:35 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\Trial folder
2024-10-05 08:23:35 - Directory created: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\Trial folder
2024-10-05 08:23:35 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\Trial folder\Image trial 1.bmp
2024-10-05 08:23:35 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Trial folder\Image trial 1.bmp -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\Trial folder\Image trial 1.bmp
2024-10-05 08:23:35 - Skipping file permissions setting on Windows for path: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\Trial folder\New Excel after a restart.xlsx
2024-10-05 08:23:35 - File updated: C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_source\Trial folder\New Excel after a restart.xlsx -> C:\Users\ASUS\Desktop\veeam_project\sync_trial\sync_trial_replica\Trial folder\New Excel after a restart.xlsx
2024-10-05 08:23:35 - Synchronization complete. Time taken: 0.02 seconds
2024-10-05 08:24:05 - Source folder contains 7 files and 1 directories.
2024-10-05 08:24:05 - Replica folder contains 7 files and 1 directories.
2024-10-05 08:24:05 - Total operations to perform: 16
2024-10-05 08:24:05 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:24:35 - Source folder contains 7 files and 1 directories.
2024-10-05 08:24:35 - Replica folder contains 7 files and 1 directories.
2024-10-05 08:24:35 - Total operations to perform: 16
2024-10-05 08:24:35 - Synchronization complete. Time taken: 0.01 seconds
2024-10-05 08:24:55 - Received interrupt signal. Exiting gracefully...
