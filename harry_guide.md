# How to emulate my workflow

There is a LOT of junk in the folder I uploaded so best to follow my directions.

This info is specific to my workflow and so it'll be missing a lot of the related information required to actually understand yolov5 and how to use it properly. There are loads of tutorials linked on the yolov5 github to help with that stuff or just ask me.

## Environment

This uses a conda env which has been specified in the environment.yaml file

run `conda env create -f environment.yml`

## Dataset
This is how I have my directory structured, but you will have to change the file paths anyway so it's probably not worth copying it.
<img width="263" alt="image" src="https://user-images.githubusercontent.com/59520303/229182657-2cae6542-50fa-4cd0-927c-d815061cd94a.png">

If you want the dataset, run:
`git clone https://github.com/hpfield/ads_dataset.git`

You will need to split it into train/test for yolov5 to work, use the notebook in preprocessing/split_folders_with_class.ipynb

## Train
Use the colab notebook in google colab:
- change the file paths to reflect your system
- do not run the cells to resize the files

## Extract feature vectors (work in the models/yolov5-master directory)
(change file path)
python classify/my_predict.py --weights gdrive_weights/calssify_224/best.pt --source '/Users/rz20505/Documents/training_year/applied_data_science/data/uob_image_set_resized/*/*.jpg' --visualize --save-txt  

Running my_predict.py will save the feature vectors in the data/ folder

## Visualise feature vectors (work in the models/yolov5-master directory)
run the vector_representations.ipynb file in the my_testing dir

## View bad predictions (work in the models/yolov5-master directory)
run the view_bad_predictions.ipynb file in the my_testing dir
