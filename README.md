# PFHCDataBase
This repository contains all the records of files related to updates in PF Hadron Calibration. TWiki: https://twiki.cern.ch/twiki/bin/view/CMS/PFCalibrationDBConditions The details of each folder is as follows:

# PDF: 
Slides/Results or related documentation with updates in PF Hadron Calibration

# textfiles: 
To store all the metadata text files

# SQLiteFiles: 
To store .db file correcspinding to the metadata text files. 

# xmlfiles
To create xml files correspoding to each Tag follow these steps in PFHCDataBase directory within CMSSW environment: 

```
conddb --db /path/fileName.db  list TagName
```
it will show unique Payload hash of the payload (simiar to this c85fdfbbca045de26ae6e641763c61c42ff6ab39). To generate xml file write:

```
conddb dump -d PFCalibration.xml PayloadHash

(for ex.) conddb dump -d PFCalibration.xml c85fdfbbca045de26ae6e641763c61c42ff6ab39
```
now xml file is ready. Note that xml should be made only after uploading db file to database.
