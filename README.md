# Leaf Segmenter and Counter

This package provides an implementation of leaf segmentation to accompany the paper 'Deep Leaf Segmentation Using Synthetic Data'.

It uses the Matterport Mask RCNN framework. Weights for a model trained on synthetic plant images (h5 file) and the images themselves (tar file) can be downloaded from https://doi.org/10.25919/5c36957c0af41.

# Setup
1. Create a virtual environment: ```python3 -m venv env```
2. Activate the environment: ```source env/bin/activate```
3. Install wheel: ```pip3 install wheel```
7. Clone the Matterport Mask RCNN implementation: ```git clone https://github.com/matterport/Mask_RCNN.git```
    - At the time of development (Jan 2019) the current version was commit: a0a2aa00f813ee61421d96b6f4c90e711b962a9d
8. Change directory into mask rcnn: ```cd Mask_RCNN```
10. Install dependencies: ```pip3 install -r requirements.txt```
11. Add Mask_RCNN to the PYTHON PATH: ```export PYTHONPATH=$PYTHONPATH:/path/to/Mask_RCNN```

# Run the segmentation
The script has a simple command line interface. Use ```--help``` for information about parameters. It will output leaf segmentations and a csv file containing the predicted count for each image.
1. ```python3 segmenter.py --dataPattern '/path/to/data/*.png' --outputDir /path/to/save/output --weightsPath /path/to/weights/leafSegmenter0005.h5 --verboseDetection --useCPU```

# Compatibility
This framework has been tested on Ubuntu 16.04.

# Contact Information
Peyman Moghadam
Peyman.Moghadam@data61.csiro.au

# Attribution / Citation / Sources
To attribute this model, please include the following citations:
## Synthetic data
For more information about the synthetic data see: https://research.csiro.au/robotics/our-work/databases/synthetic-arabidopsis-dataset/
```
Ward, Daniel; Moghadam, Peyman (2018): Synthetic Arabidopsis Dataset. v4. CSIRO. Data Collection. 
https://doi.org/10.25919/5c36957c0af41
```

## Paper
```
D. Ward, P. Moghadam, and Nicolas Hudson, "Deep Leaf Segmentation Using Synthetic Data", British Machine Vision Conference (BMVC) Workshop on Computer Vision Problems in Plant Pheonotyping (CVPPP 2018)
```
## Paper (bibtex)
```
@article{ward2018deep,
  title={Deep leaf segmentation using synthetic data},
  author={Ward, Daniel and Moghadam, Peyman and Hudson, Nicolas},
  journal={arXiv preprint arXiv:1807.10931},
  year={2018}
}
```

## Mask RCNN Framework (from the matterport readme)
```
@misc{matterport_maskrcnn_2017,
  title={Mask R-CNN for object detection and instance segmentation on Keras and TensorFlow},
  author={Waleed Abdulla},
  year={2017},
  publisher={Github},
  journal={GitHub repository},
  howpublished={\url{https://github.com/matterport/Mask_RCNN}},
}
```