# yolov5-cyclist-detection

This repository contains a notebook for a coursework project which involves creating a subsample of a larger dataset, splitting it into training, validation, and testing sets, and then training a model using YOLOv5. 

The script primarily operates on a dataset located at `/INM705/705 Coursework/datasets/data_tsinghua` where images are in `images` subdirectory and labels are in `labels` subdirectory.

## File Structure 

The directory structure for this project is as follows:

```
/
└── INM705/
    └── 705 Coursework/
        ├── datasets/
        │   ├── data_tsinghua/
        │   │   ├── images/
        │   │   └── labels/
        │   └── cyclist_data/
        ├── sample_data/
        │   ├── labels_zero/
        │   ├── labels_sample/
        │   └── images_sample/
        └── yolov5/
```

## Dependencies

To run this code, you will need the following dependencies:

- Python 3.x
- os
- pathlib
- random
- glob
- YOLOv5
- torch
- IPython
- yaml
- matplotlib

You can install these packages with pip:

```bash
pip install os pathlib random glob torch ipython yaml matplotlib
```

YOLOv5 can be installed by running:

```bash
pip install -U git+https://github.com/ultralytics/yolov5.git
```

After cloning the YOLOv5 repository, navigate to the yolov5 directory and run:

```bash
pip install -r requirements.txt
```

## Running the Code

Before running the code, you should replace the placeholders (`"/users/addj212/INM705/705 Coursework"`) with the correct directory path on your machine.

After setting up the directory, you can simply run the Python script from the command line. It will first create a subsample of the original dataset. It then prepares the data for YOLOv5 by splitting it into train, validation, and test sets. Finally, the code trains the model using YOLOv5.

The output of the training will be saved to the 'Runs' folder.

## Support

Please raise an issue on the GitHub repository if you encounter any problems while running the script. Please provide as much detail as possible, including error messages and your environment setup. 

## Disclaimer

This code is intended to be run in an environment that uses the same directory structure as outlined above. If your directory structure differs, please adjust the paths in the code to match your structure. 

Additionally, this code is designed to be run on the Hyperion system with the specific dataset noted above. If you wish to use it with a different dataset or system, modifications may be necessary.

## Credits

This project makes use of the YOLOv5 library, which can be found here (https://github.com/ultralytics/yolov5). File operations were learned from 'The Quick Python Handbook' by Ceder (2018), and the model setup was adapted from this [Towards Data Science guide] (https://towardsdatascience.com/the-practical-guide-for-object-detection-with-yolov5-algorithm-74c04aac4843).
