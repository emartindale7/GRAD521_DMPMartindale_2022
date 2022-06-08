# Research Overview

The research covered in this plan is to develop a machine learning model that can accurately classify the sleep states of mice based on noninvasively collected data. The mice will be observed while they are in an environment that they are familiar with. They will be observed using electric field sensors which can measure movement of the mice from outside of their cage. This data will be used to classify periods that the mice are resting into three stages, wake, REM, and NREM. The research question that this project will be answering is "what features of the electric field signal are important to accurately classify sleep stages?". 

# Data description

For this research project, data will need to be collected using electric field sensors and from camera above the cages. Video from the camera will be used to verify sleep/ wake states of the mice that are scored using the electric field data. The electric field sensor and video data will be collected by observing the mice in their cages without any outside interference or distractions to see how the mice act when they are not stressed. The original data files of electric field data are saved as proprietary .abf files and the video files are saved as .avi files. 

A subset of data is manually scored by using Spike2 software to view the abf files and ELAN software to view the video files. Both programs are then used to produce annotations for the electric field sensor or camera data and output these annotations, or scores, as mat files. MATLAB scripts have been written to then process the abf files and mat files into combined mat files with data organized into 10 second epochs. This can then be further processed with another MATLAB script to produce a single csv of extracted features from many input files. Python scripts then take this csv as input to train machine learning models with. The MATLAB and python scripts are being developed throughout this project to produce an acceptable classification model and will be managed with this data management plan. 

The electric field dataset is estimated to be between 0.5 and 1 GB and the combined electric field and scoring dataset is estimated to be about 1 GB. The video dataset is estimated to be about 100 GB. The processed data is estimated to be about 3.5 GB. The total size of the datasets is then estimated to be about 115 GB.

# Roles and responsibilities

Everyone involved in data collection and processing is responsible for implementing the data management plan. The PI for the lab is responsible for making sure that there is a data management plan and that people are following it. The PI will also be in charge of making sure the data is being properly archived, preserved and also making sure to protect sensitive and protected data, and overall access control of all data. The lead grad student for each project will be in charge of coming up with a consistent data organization plan, making sure the proper metadata is being generated and recorded, and the data management for that project. All other grad students involved in the project will hep to ensure instruments are in calibration and have proper maintenance recorded, creating and maintaining useful software and code, and working on data analysis. Anyone generating or collecting data is responsible for quality control, though the lead grad student and PI are responsible for overall quality control of the project.

The data is not sensitive or confidential according to OSU’s policy. The unrestricted data stills needs to be in a secure location though to make sure data is not lost. This will be done by using an Oregon State approved data storage location, especially for any data that will be remotely accessible.

Data will be first collected and stored on the lab computer that runs the equipment. When a set of data has been collected it will be copied to an external hard drive to be transferred and kept with the rest of the project data. For data processing and analysis, copies of the data will be transferred to a workstation to perform any processing and analysis needed. The original files will not be changed and the newly created files will need to be copied to the overall project storage location. If this data is going to be accessed from multiple computers for these steps copies may be saved to an Oregon State cloud service but then any generated data will need to be saved in the same location as the original data. 

The centralized storage of data prevents any data being lost if a researcher were to leave the project. Backups of this centralized data will be done manually as the original, raw data will only be added to and will not be modified and all of the future forms of data will be added periodically. Any process that produces new data will either be from manual scoring or automated processing from MATLAB and python scripts. These data will be stored in the central storage location as each set of data is processed to limit any potential data loss. 

# Data standards and metadata

Data and scripts produced under this plan will fall into three different categories.  

- Dataset 1: Original, raw data files. 

  Electric field files and video files are collected and saved to project specific folders that are named for the experiment, the date, the cage, and the animals. The individual files follow the same naming convention and structure to ensure they are not misplaced and data is not lost. Files are stored in a structure of experiment/ experiment_date/ experiment_date_cage_animals with the files being named experiment_date_cage_animals. An example of this would be PVA EXP_01-01-2020_Cage1_AL&AR-0001.abf/ .avi. 

- Dataset 2: Processed data and model outputs. 

  When the data is to be manually analyzed, the raw files are loaded into a either Spike2 for abf files or ELAN for video files and then the labeled and processed output is saved as a new filetype and named with the same naming convention. The raw and manually processed data can then be input into the MATLAB scripts being developed under this project and the output will include the same naming convention with an appended marker to denote the stage of processing that has been done. 

- Dataset 3: Processing and machine learning scripts.

  Metadata for the project code can be found in the [codemate.json](codemeta.json) file which uses the [CodeMeta Project](https://codemeta.github.io/) as a standard to describe the code itself. Git version control is used to record the different iterations of software developed for this project. A local git repository will be used while the software and analysis tools are still in development, but when the project is finished, this repository will be published along with the information collected. This version control will also be used to record the documentation files that are written to explain the software analysis and describe the necessary metadata.

There is no current metadata standard for the field to describe the first two datasets. Metadata on the methods to collect this data is shown in published work by [Kloefkorn et al](https://doi.org/10.1016/j.jneumeth.2020.108834)[^1].

# Storage and security

The data for this research project is stored and backed up with external hard drives in two different places. The backup process is then currently done manually and does not involve any specific programs or a network drive. Any data that is saved to a cloud system should also be backed up to a hard drive so that the lab retains all of the data for the project. The cloud folders for any ongoing research are also owned by the lab PI so that if any data would not have been backed up yet, they will not be lost when a student graduates.

# Access and data sharing

The sharing and use of the data is not restricted by any factors. The data will be licensed under CC BY  so that anyone can use the data as long as they give credit to the researchers that collected the data. Data will be available in the associated paper under supplementary data. The paper will also provide a link to where the data is stored in the [Zenodo](https://zenodo.org/) repository. If there are problems accessing data from the repository or from the supplemental data with the paper, contact information given in the paper can be used to notify the lab of the problem and directly request copies of the data. 

GitHub will be used to publish the code repository of the MATLAB and python scripts, which will also be linked to in the paper. This code repository will also be integrated into the Zenodo repository according to the archiving and preservation section of this plan. 

# Archiving and preservation

The data for this project and the scripts developed throughout will be archived and preserved in the Zenodo repository. This repository aims to retain data indefinitely and if they cannot, will migrate the dataset and associated files to another repository that can. There will also be copies of the data and scripts retained by the lab for 5 years in the lab's storage location. The MATLAB and python scripts will also maintained in GitHub with new versions to allow more use for different file types and parameters to use. 

# References

[^1]: Kloefkorn, H., Aiani, L. M., Lakhani, A., Nagesh, S., Moss, A., Goolsby, W., Rehg, J. M., Pedersen, N. P., & Hochman, S. (2020). Noninvasive three-state sleep-wake staging in mice using electric field sensors. *Journal of Neuroscience Methods*, *344*, 108834. https://doi.org/10.1016/j.jneumeth.2020.108834  
