APTrustHelper is a small Java GUI application which assists with transmitting files downloaded from a DSpace repository to APTrust.

Prerequisites
=============
Before using the program, you'll need the following.
1. The bagit-java executable, downloaded from https://github.com/LibraryOfCongress/bagit-java.
2. The AP Trust helper tools (Windows only), downloaded from https://sites.google.com/a/aptrust.org/aptrust-wiki/home/partner-tools.
3. A valid configuration file which contains the credentials needed to conect to AP Trust. See https://sites.google.com/a/aptrust.org/aptrust-wiki/home/partner-tools for more details on how the config file should be constructed.

How To Use
==========
1. Click the aptrusthelper_clickable.jar file to start the application.
2. Set up the locations of your bagit-java executable, AP Trust tools, and configuration file using the buttons on the GUI. You'll need to set these locations up only once unless they change.
3. Use the "Show Receiving Bucket" button to list the current files in your receiving bucket.
4. If you want to upload a DSpace item, first download it from DSpace. Select the downloaded zip file, choose a bag name, and prefix, and click the 'Upload' button.

What Upload Does
================
1. Unzips the DSpace zip file.
2. Uses bagit-java to create a bag of the zip file contents.
3. Name the bag using the institutional prefix and handle from the DSpace handle file.
4. Add the aptrust-info.txt file to the bag.
5. Validate the bag using the AP Trust tools.
6. If the bag passes validation, upload the bag using the AP Trust tools.

Current Issues and Limitations
==============
1. When uploading bags, the program is currently throwing an error about getting an MD5 receipt. However, the file does upload successfully.
2. Eventually the bagit-java code could be integrated rather than used as a separate program.
3. Works with Windows only.
2. Works only with single-item zip files exported directly from a DSpace 4 or 5 repository.
