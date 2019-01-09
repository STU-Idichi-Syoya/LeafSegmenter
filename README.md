# Leaf Segmenter and Counter
This script runs leaf segmentation using the Matterport Mask RCNN framework with supplied weights.

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
1. ```python3 segmenter.py --dataPattern '/path/to/data/*.png' --outputDir /path/to/save/output --weightsPath /path/to/weights/mask_rcnn_cvppp_0002.h5 --verboseDetection --useCPU```

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
Ward, Daniel; Moghadam, Peyman (2018): Synthetic Arabidopsis Dataset. v3. CSIRO. Data Collection. https://doi.org/10.25919/5b68e64547015
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