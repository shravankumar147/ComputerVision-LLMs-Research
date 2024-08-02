# Downstream-Dino-V2

Welcome to the Downstream-Dinov2 repository! This project provides an easy-to-use implementation of the DINOv2 model developed by Facebook, allowing you to train it for downstream tasks effectively.

## ToDo
✅ Add classification model <br />
✅ Add training and inference code for classification model <br />
✅ Add exapmle notebook <br />
✅ Add segmentation model <br />
✅ Add training code for segmentation model <br />
✅ Add Segmentation model to the example notebook <br />
☐ Refactot the code for segmentation and add comments <br />

The DINOv2 model used in this project is originally developed by Facebook AI and can be found at facebookresearch/dinov2.

## Requirements

All the dependencies can be installed using the provided requirements.txt file.

## Installation

1. Clone the repository:

   ```
   git clone https://github.com/itsprakhar/Downstream-Dinov2
   ```

2. Change the directory:

   ```
   cd Downstream-Dino-V2
   ```

3. Create a conda environment and install dependencies:

   ```
    conda create --name dinov2 --file requirements.txt
   ```

4. Activate the conda environment:

   ```
   conda activate dinov2
   ```

## Calssification Usage

Prepare your dataset and place it in the `data/train` directory. The data should be structured such that each class has its own subdirectory containing the respective images. Run the training script with:

```
python train_classifier.py
```

Note: This will use the smallest DinoV2 model to use any other, you can change this part in the train_classifier.py code

```
model = Classifier(num_classes) # this will load the small model
# model = Classifier(num_classes, backbone = 'dinov2_b') # to load the base model
# model = Classifier(num_classes, backbone = 'dinov2_l') # to load the large model
# model = Classifier(num_classes, backbone = 'dinov2_g') # to load the largest model
```

This will train the model for 100 epochs (modifiable in the script), using the DINOv2 model as a feature extractor and a custom classifier. The training process includes data augmentation, training/validation splitting, and early stopping.

## Demo

A demo notebook is provided to guide you on how to use the trained model to classify images. The notebook demonstrates how to load the model, preprocess an image, and perform inference. Check out the `demo.ipynb` file in the repository.

## License

DINOv2 code and model weights are released under the CC-BY-NC 4.0 license. See LICENSE for additional details.

## Contact

Prakhar Thakur - itsprakharthakur@gmail.com

Project Link: https://github.com/itsprakhar/Downstream-Dinov2

Please ⭐ if you find it useful so that I find the motivation to keep improving this. Thanks
