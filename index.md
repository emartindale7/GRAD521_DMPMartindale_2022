# Data description

The research that I will be working on involves observing mice in their cages to see how they react in a familiar environment over the course of a study. 
The mice will be observed using an electric field sensor and this data will be used to develop a machine learning model that can automatically sort the data into different wake or sleep stages. 
The specific research question this project will be answering is how well can a machine learning system predict the activity of mice. 

For this research question, I will need to collect data from the electric field sensors and from a secondary source such as a video of the cages. 
The video will be used to verify sleep/ wake states of the mice that are scored using the electric field data. 
The electric field sensor and video data will be collected by observing the mice in their cages without any outside interference or distractions to see how the mice act when they are not stressed. 
The original data set of electric field data will be scored in 10 second increments before being used to train the machine learning system. 
The electric field data contains voltage readings with timestamps and metadata of the sampling rate, file name, and other sampling parameters. 
The sleep scoring data is then created with another program to view the electric field data and saved in a combined file with the original data. 
The video files are viewed separately to verify the scoring, but are not saved in the combined file. 
The combined electric field and scoring data is processed to prepare it for the machine learning system and this is saved in a new file format. 

The electric field dataset is estimated to be between 0.5 and 1 GB and the combined electric field and scoring dataset is estimated to be about 1 GB. 
The video dataset is estimated to be about 100 GB. 
The processed data is estimated to be about 3.5 GB. 
The total size of the datasets is then estimated to be about 115 GB. 

# Roles and responsibilities

Everyone involved in data collection and processing is responsible for implementing the data management plan. 
The PI for the lab is responsible for making sure that there is a data management plan and that people are following it. 
The PI will also be in charge of making sure the data is being properly archived, preserved and also making sure to protect sensitive and protected data, and overall access control of all data. 
The lead grad student for each project will be in charge of coming up with a consistent data organization plan, making sure the proper metadata is being generated and recorded, and the data management for that project. 
All other grad students involved in the project will hep to ensure instruments are in calibration and have proper maintenance recorded, creating and maintaining useful software and code, and working on data analysis. 
Anyone generating or collecting data is responsible for quality control, though the lead grad student and PI are responsible for overall quality control of the project.

The data is not sensitive or confidential according to OSU's policy. 
The unrestricted data stills needs to be in a secure location though to make sure data is not lost. 
This will be done by using an Oregon State approved data storage location, especially for any data that will be remotely accessible. 

Data will be first collected and stored on the lab computer that runs the equipment. 
When a set of data has been collected it will be copied to an external hard drive to transfer and kept with the rest of the data. 
for data processing and analysis the drives with the required data will be connected to a computer for the processing and analysis. 
If this data is going to be accessed from multiple computers for these steps copies may be saved to an Oregon State cloud service but then any generated data will be saved in the same location as the original data. 

The data for this research project is stored and backed up with external hard drives in two different places. 
The backup process is then currently done manually and does not involve any specific programs or a network drive. 
Any data that is saved to a cloud system should also be backed up to a hard drive so that the lab retains all of the data for the project. 
The cloud folders for any ongoing research are also owned by the lab PI so that if any data would not have been backed up yet, they will not be lost when a student graduates. 

# Data standards and metadata

Data for this project is organized using a file naming convention and file structure. 
Electric field files and video files are collected and saved to project specific folders that are named for the experiment, the date, the cage, and the animals. 
The individual files follow this same naming convention to ensure they are not misplaced and data is not lost. 
When the data is to be manually analyzed, the raw files are loaded into a program and the labeled and processed output is saved as a new filetype and named with the same naming convention. 
The raw and manually processed data can then be input into the software that is being developed for this project and the output will include the same name, but with a signifier appended to the end to denote at what stage of the automatic analysis the output files are from.

Git version control is used to record the different iterations of software developed for this project. 
A local git repository will be used while the software and analysis tools are still in development, but when the project is finished, this repository will be published along with the information collected. 
This version control will also be used to record the documentation files that are written to explain the software analysis and describe the necessary metadata. 

There is not currently a metadata standard being used for this project. 
A current standard that would likely be applicable for this project is the [ISA-Tab](http://isatab.sourceforge.net/docs/ISA-TAB_release-candidate-1_v1.0_24nov08.pdf) standard. 
This standard guides organization of file structure so that complex information from a specific assay or test can be related back to a study and that study can be related back to the larger investigation. 

# Storage and security

# Access and data sharing

# Archiving and preservation
