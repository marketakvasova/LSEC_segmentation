# LSEC_segmentation

This repository includes Jupyter Notebooks for Google Colab. 
These notebooks are intended to automatically segment fenestrations in LSECs.

This repository includes a notebook for creating segmentation masks of fenestrations: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/marketakvasova/LSEC_segmentation/blob/main/LSEC_fenestration_segmentation.ipynb).

The model was trained using this script: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/marketakvasova/LSEC_segmentation/blob/main/automatic_image_segmentation.ipynb).

Some attempts were made to create segmentation masks of whole cells using the Segment Anything model.: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/marketakvasova/LSEC_segmentation/blob/main/semiautomatic_cell_segmentation.ipynb).
These attempts were not very successful, as the model works only sometimes(when there is a good contrast between the cell and the background).
The Segment Anything Model downscales the image quite a lot because the SEM images are very large.
This means a lot of information about the cell edges is lost.
The task of segmenting the cells themselves is probably more difficult than segmenting fenestrations because of the large image size and unclear cell edges.
