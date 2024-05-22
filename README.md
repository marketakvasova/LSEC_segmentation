# LSEC_segmentation

This repository includes Jupyter Notebooks for Google Colab. 
These notebooks are intended to automatically segment fenestrations in LSECs.

This repository includes a notebook for creating segmentation masks of fenestrations: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/marketakvasova/LSEC_segmentation/blob/main/LSEC_fenestration_segmentation.ipynb).
You can either run the script in Google Colab (this allows you to use Google's GPU, but you have to upload your data to Google Drive).
Or you can download it and run it on your PC (for example in VS Code https://code.visualstudio.com/).

If you are running it on your PC, follow these steps:

1. Download Python https://www.python.org/downloads/. (When the first window appears during installation, check the "Add python.exe to PATH" box at the bottom!)
2. Install necessary libraries
   - On Windows:<br>
     do this by downloading the file install_libraries_win.bat and running it by double-clicking on it.<be>
     (Windows might give you some warnings when you try to run it, but you can check the file contents here on GitHub.)
   - other OS:
     download install_libraries.sh<br>
     in terminal run:<br>
     chmod +x install_libraries.sh<br>
     ./intstall_libraries.sh
          
4. Download some IDE, where you can run the script (e.g. https://code.visualstudio.com/).

The individual cells are executed by clicking on the arrows on their left side (Execute cell).
When you try to run it in VSCode for the first time, VSCode will suggest installing the necessary extensions for the script (Python+Jupyter).
<br>

The model was trained using this script: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/marketakvasova/LSEC_segmentation/blob/main/automatic_image_segmentation.ipynb).

Some attempts were made to create segmentation masks of whole cells using the Segment Anything model.: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/marketakvasova/LSEC_segmentation/blob/main/semiautomatic_cell_segmentation.ipynb).
These attempts were not very successful, as the model works only sometimes(when there is a good contrast between the cell and the background).
The Segment Anything Model downscales the image quite a lot because the SEM images are very large.
This means a lot of information about the cell edges is lost.
The task of segmenting the cells themselves is probably more difficult than segmenting fenestrations because of the large image size and unclear cell edges.
