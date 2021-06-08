Title : A Deep Learning Approach to JPEG Compressed Document Image Quality Assessment

1) 
Copy the dataset and put all images in a directory and set this directory as `root` in 'config.yaml'

2)
The ground truth for the dataset has been pre-processed and saved as a excel file `SOC_gt.xlsx` stored in `./data/gt_files/SOC_gt.xlsx`

3)
The ground truth file contains:
- img_name: the image name
- img_set: the index of reference image from which the current compressed image is generated.
- acc_avg: average accuracy of Tesserect Engine and Manual Verification


4)
Training and validating
python main.py --batch_size=128 --epochs=500 --lr=0.001

5)
demo_DIQA
python demo_DIQA.py

6)
When a DIQA model has been trained, `demo_DIQA.py` can be used to predict the quality of a document image directly.

7)
Before running `demo_DIQA.py`, the `model_path` and `img_path` must be specified.
