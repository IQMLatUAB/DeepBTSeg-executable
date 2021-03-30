# DeepBTSeg-executable
[![IQMLatUAB - DeepBTSeg-executable](https://img.shields.io/static/v1?label=IQMLatUAB&message=DeepBTSeg-executable&color=blue&logo=github)](https://github.com/IQMLatUAB/DeepBTSeg-executable)
[![Developed - MATLAB 2020b](https://img.shields.io/badge/Developed-MATLAB_2020b-blueviolet?logo=Mathworks&logoColor=white)](https://)
[![stars - DeepBTSeg-executable](https://img.shields.io/github/stars/IQMLatUAB/DeepBTSeg-executable?style=social)](https://github.com/IQMLatUAB/DeepBTSeg-executable)
[![forks - DeepBTSeg-executable](https://img.shields.io/github/forks/IQMLatUAB/DeepBTSeg-executable?style=social)](https://github.com/IQMLatUAB/DeepBTSeg-executable)

DeepBTSeg provides a user-friendly graphical user interface (GUI) of remote state-of-the-art deep learning models, which allow users to conduct deep learning  brain tumor image segmentation without the cumbersome of both software and hardware requirements on users' local computers. 

This repository is the client end executable version of DeepBTSeg. We also provide Matlab code of DeepBTSeg [here](https://github.com/IQMLatUAB/DeepBTSeg).
DeepBTSeg is **developed under Matlab 2020b** and is **executable under Matlab 2019b and Matlab 2020a**.
# Usage
## Contents
- [Install](#Install)
- [User_Instruction](#User_Instruction)
## Install
> Windows version (developed under Matlab 2020b)

1. Dowload DeepBTSeg repository and unzip it. 

![](images/9.png)

2. Double click DeepBTSeg.exe.

![](images/1.PNG)

3. Click "Next" 

![](images/2.PNG)

4. Click "Next" 

![](images/3.PNG)

5. Click "Next" 

![](images/4.PNG)

6. Select "Yes" and "Next"

![](images/5.PNG)

7. Click "install"

![](images/6.PNG)
![](images/7.PNG)

8. Installation is completed!

## User_Instruction
1. `ATTENTION！`Right click and choose `run as administrator` all the time (even you log in as administrator in your computer). Then, the `DeepBTSeg_GUI` will appear.

![](images/8.png)
![](images/DeepBTGUI_whole_window.PNG)

2. Click `Load images` button select the DICOM folder which needed to be processed.

3. Parse the directory of DICOM images. Under the `Select as` column, specify `T1pre`, `T1post`, `T2`, `Flair` to the corresponding series, then click `OK`.
![](images/DICOM_selection.png)

4. Back to `DeepBT_GUI`, select the desired model that wants to be used during the segmentation process.

5. Click `Submit job for selected model` to transmit this job to the server for processing or click “Submit jobs for all models” to apply all models on the current DICOM image series.

    - Then, the series and the selected model will be composed to a job, then be moved to the lower `Jobs` panel. And, the `Status` will become `Submitted`.

6. Click `Check job` under the `Action` column or `Update status for all jobs` button to refresh the job status and messages from the server, which shown in matlab command window.
    - If the Job is finished, server will send the result back to the client, then `Status` column will change from `Submitted` to `Completed`.

7. After the Job is completed, the user can view the result by click the `View results` option under `Action` column.

![](images/Image_viewer.png)

8. The above image is a pop-up `image viewer`. Ther are several finction we implemented.
    - User can choose which ROI they want to investigate by clicking the axial, sagittal, coronal sliced images.
    - User can click which segmented label of brain tumor contour they want to explore.
    - User can also switch the different series (T1, T1post, T2, Flair)
    - If user wnat to export this segment result, they can push `Export results as DICOM RTSS` button. Then, the `Action` will become `Exported` in the `DeepBTSeg_GUI`.

9. In `DeepBTSeg_GUI`, click `Export results` under the `Action` column can also save processing results as DICOM RTSS file. 

> when the job status is "Completed". Make sure you export results before you close DeepBTSeg because non-save results will be automatically eliminated.
# Future Work
Right now, we are still working on to implement more DL models on the server so that the user can have more options to segment the brain tumor.

# Maintainer
[@IQMLatUAB](https://github.com/IQMLatUAB)

[@Zi-Min Weng](https://github.com/elite7358)

[@Sheng-Chieh Chiu](https://github.com/chocolatetoast-chiu)
